<template>
  <div class="tab" v-bind="TabMenu">
    <button
      id="aboutus"
      class="tablinks"
      v-on:click="onclick()"
      style="border-bottom-color: white"
    >
      ABOUT US
    </button>
    <button id="blogs" class="tablinks" v-on:click="onclick()">BLOGS</button>
    <button id="careers" class="tablinks" v-on:click="onclick()">
      CAREERS
    </button>
    <button id="contact" class="tablinks" v-on:click="onclick()">
      CONTACT
    </button>
    <div id="aboutusdiv" class="tabcontent" style="display: inline-block">
      <h4>Header1</h4>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ipsa
        reiciendis nisi suscipit dicta cumque itaque obcaecati eligendi natus
        praesentium eaque.
      </p>
      <h4>Header</h4>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ipsa
        reiciendis nisi suscipit dicta cumque itaque obcaecati eligendi natus
        praesentium eaque.
      </p>
      <h4>Header</h4>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ipsa
        reiciendis nisi suscipit dicta cumque itaque obcaecati eligendi natus
        praesentium eaque.
      </p>
    </div>

    <div id="blogsdiv" class="tabcontent">
      <h4>Header2</h4>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ipsa
        reiciendis nisi suscipit dicta cumque itaque obcaecati eligendi natus
        praesentium eaque.
      </p>
      <h4>Header</h4>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ipsa
        reiciendis nisi suscipit dicta cumque itaque obcaecati eligendi natus
        praesentium eaque.
      </p>
      <h4>Header</h4>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ipsa
        reiciendis nisi suscipit dicta cumque itaque obcaecati eligendi natus
        praesentium eaque.
      </p>
    </div>

    <div id="careersdiv" class="tabcontent">
      <h4>Header3</h4>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ipsa
        reiciendis nisi suscipit dicta cumque itaque obcaecati eligendi natus
        praesentium eaque.
      </p>
      <h4>Header</h4>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ipsa
        reiciendis nisi suscipit dicta cumque itaque obcaecati eligendi natus
        praesentium eaque.
      </p>
      <h4>Header</h4>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ipsa
        reiciendis nisi suscipit dicta cumque itaque obcaecati eligendi natus
        praesentium eaque.
      </p>
    </div>
    <div id="contactdiv" class="tabcontent">
      <h4>Header4</h4>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ipsa
        reiciendis nisi suscipit dicta cumque itaque obcaecati eligendi natus
        praesentium eaque.
      </p>
      <h4>Header</h4>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ipsa
        reiciendis nisi suscipit dicta cumque itaque obcaecati eligendi natus
        praesentium eaque.
      </p>
      <h4>Header</h4>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ipsa
        reiciendis nisi suscipit dicta cumque itaque obcaecati eligendi natus
        praesentium eaque.
      </p>
    </div>
  </div>
</template>

<style>
.tab {
  background-color: #383838;
  color: white;
  margin: 1% auto 0% auto;
  width: 40%;
  height: 70vh;
}

/* Style the buttons inside the tab */
.tab button {
  display: inline-block;
  border-top: none;
  border-left: none;
  border-right: none;
  outline: none;
  cursor: pointer;
  padding: 14px 16px;
  transition: 0.3s;
  font-size: 17px;
  color: white;
  background-color: #383838;
}

/* Change background color of buttons on hover */
.tab button:hover {
  background-color: #383838;
}

/* Create an active/current tablink class */
.tab button.active {
  border-bottom: 2px;
  border-bottom-color: white;
}

.tabcontent {
  display: none;
  margin: 5%;
  text-align: left;
  color: white;
}
</style>



<script>
export default {
  name: "TabMenu",
  methods: {
    onclick: function () {
      let idx;
      let btn = document.getElementsByTagName("button");
      for (let i = 0; i < btn.length; i++) {
        btn[i].onclick = function () {
          idx = this.id;
          let dividx = this.id + "div";
          document.getElementById(dividx).style.display = "inline-block";
          document.getElementById(idx).style.borderBottomColor = "white";
          document.getElementById(idx).style.backgroundColor = "grey";
        };
      }
      for (let i = 0; i < btn.length; i++) {
        if (btn[i].id != idx) {
          btn[i].style.backgroundColor = "#383838";
          btn[i].style.borderBottomColor = "#383838";
        }
      }
      let tabcontent = document.getElementsByClassName("tabcontent");
      for (let i = 0; i < tabcontent.length; i++) {
        tabcontent[i].style.display = "none";
      }
    },
  },
};
</script>