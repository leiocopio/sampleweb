<script>
    import "../app.css";


    const darkMode = (event) => {
        //document.body.classList.toggle("dark");
        if (event.target.checked) {
        console.log("dark mode");
        document.body.classList.add("dark-mode");
            
        } else {
        document.body.classList.remove("dark-mode");

    }}
</script>

<label class="switch">
    <input type="checkbox" on:click={darkMode} hidden>
    <span class="slider"></span>
  </label>

<style>

.switch {
  position: relative;
  display: inline-block;
  width: 60px;
  height: 34px;
  border-radius: 50%;
}

.slider /*
    Background color of switch
*/{
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #68B7DE;
  -webkit-transition: .4s;
  transition: .4s;
  border-radius: 30px;
  
}

.slider:before {
  position: absolute;
  content: "";
  height: 26px;
  width: 26px;
  left: 4px;
  bottom: 4px;
  background-color: #F4D06F; 
  -webkit-transition: .4s;
  transition: .4s;
  border-radius: 30px;
}

input:checked + .slider {
  background-color: #191970;
}

input:focus + .slider {
  box-shadow: 0 0 1px #191970;
}

input:checked + .slider:before {
  -webkit-transform: translateX(26px);
  -ms-transform: translateX(26px);
  transform: translateX(26px);
  background-color: #ccc;
}
</style>