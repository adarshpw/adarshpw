<!DOCTYPE html>
<html>
<head>
<style>
  .scene {
    width: 200px;
    height: 200px;
    perspective: 400px;
  }

  .cube {
    width: 100%;
    height: 100%;
    position: relative;
    transform-style: preserve-3d;
    animation: rotate 5s infinite linear;
  }

  .cube div {
    position: absolute;
    width: 196px;
    height: 196px;
    border: 2px solid #fff;
    line-height: 196px;
    font-size: 40px;
    font-weight: bold;
    color: #fff;
    text-align: center;
    background-color: rgba(255, 255, 255, 0.3);
  }

  .front  { transform: translateZ(100px); }
  .back   { transform: rotateY(180deg) translateZ(100px); }
  .right  { transform: rotateY(90deg) translateZ(100px); }
  .left   { transform: rotateY(-90deg) translateZ(100px); }
  .top    { transform: rotateX(90deg) translateZ(100px); }
  .bottom { transform: rotateX(-90deg) translateZ(100px); }

  @keyframes rotate {
    from { transform: rotateY(0deg); }
    to { transform: rotateY(360deg); }
  }
</style>
</head>
<body>

<div class="scene">
  <div class="cube">
    <div class="front">Front</div>
    <div class="back">Back</div>
    <div class="right">Right</div>
    <div class="left">Left</div>
    <div class="top">Top</div>
    <div class="bottom">Bottom</div>
  </div>
</div>

</body>
</html>
