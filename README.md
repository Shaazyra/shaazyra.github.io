<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>TNB AR Walkthrough</title>
    <script src="https://cdn.jsdelivr.net/npm/aframe@1.2.0/dist/aframe.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/mind-ar@1.1.4/dist/mindar-image-aframe.prod.js"></script>
    <style>
      body { margin: 0; overflow: hidden; }
    </style>
  </head>
  <body>
    <mindar-image-scene image-target-src="target.mind" color-space="sRGB" embedded>
      <a-assets>
        <a-asset-item id="tnbModel" src="model.glb"></a-asset-item>
        <audio id="audio" src="audio.mp3"></audio>
      </a-assets>

      <a-entity mindar-image-target="targetIndex: 0">
        <a-gltf-model src="#tnbModel" position="0 0 0" scale="0.1 0.1 0.1" rotation="0 180 0"></a-gltf-model>
        <a-sound src="#audio" autoplay="true" position="0 0 0"></a-sound>
      </a-entity>
    </mindar-image-scene>
  </body>
</html>