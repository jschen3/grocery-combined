<script>
    export let value = "Aug 01";
    export let left = 200;
  
    let width = 50;
    let height = 15;
  </script>
  
  <div
    class="arrowBox"
    style="--after-border: {height / 2}px; --after-margin-left: {-height /
      2}px; width: {width}px; height: {height}px; line-height: {height}px; left: {left -
      width / 2}px"
  >
    {value}
  </div>
  
  <style>
    .arrowBox {
      z-index: 10;
      background-color: #000;
      border-radius: 2px;
      position: absolute;
      font-size: 0.725em;
      font-weight: 200;
      color: white;
      text-align: center;
      left: 500px;
    }
  
    .arrowBox:after {
      content: " ";
      z-index: 10;
      width: 0px;
      height: 0px;
      border-top: var(--after-border) solid #000;
      border-left: var(--after-border) solid transparent;
      border-bottom: var(--after-border) solid transparent;
      border-right: var(--after-border) solid transparent;
      border-radius: 2px;
      position: absolute;
      right: 50%;
      top: 100%;
      margin-right: -7.5px;
    }
  </style>