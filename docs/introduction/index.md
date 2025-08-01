<!DOCTYPE html>
<script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
<script src="https://raw.githack.com/AR-js-org/AR.js/master/aframe/build/aframe-ar.js"></script>

<body style="margin: 0">
  <a-scene embedded arjs="trackingMethod: best">
    <!-- Question -->
    <a-text value="ما المقصود بصعوبات التعلم؟" position="0 0.5 0" color="black"></a-text>
    
    <!-- Options as buttons -->
    <a-box position="-0.5 0 0" color="blue" onclick="checkAnswer(1)">
      <a-text value="تأخر عقلي شديد" position="0 0 0.51" color="white"></a-text>
    </a-box>
    <!-- Add other options similarly -->
    
    <!-- Score/Time -->
    <a-text id="score" value="Score: 0" position="-0.5 -0.5 0"></a-text>
  </a-scene>

  <script>
    let score = 0;
    function checkAnswer(option) {
      if (option === 3) score += 10; // Correct option
      document.getElementById('score').setAttribute('value', `Score: ${score}`);
    }
  </script>
</body>
 




