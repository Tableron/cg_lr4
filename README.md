<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>3D Сцена из Blender</title>
    <script src="https://aframe.io/releases/1.7.0/aframe.min.js"></script>
</head>
<body>
    <a-scene 
        renderer="antialias: true; 
                 shadow: true;
                 shadowMapType: pcfsoft">
        
        <a-assets>
            <a-asset-item id="blenderModel" src="models/model.glb"></a-asset-item>
        </a-assets>
        
        <a-entity 
            gltf-model="#blenderModel"
            enhance-shadows
            position="0 2 -8"
            scale="2 2 2"
            shadow="cast: true; receive: true"
            animation="property: rotation; to: 0 -360 0; loop: true; dur: 30000; easing: linear">
        </a-entity>
        
        <a-entity light="type: ambient; color: #FFF; intensity: 0.4"></a-entity>
        <a-entity light="type: directional; 
                        intensity: 3;
                        castShadow: true;
                        shadowMapWidth: 2048;
                        shadowMapHeight: 2048;
                        shadowBias: -0.0001;
                        shadowCameraLeft: -15;
                        shadowCameraRight: 15;
                        shadowCameraTop: 15;
                        shadowCameraBottom: -15;"
                 position="5 5 0">
        </a-entity>
        
    </a-scene>
</body>
</html>
