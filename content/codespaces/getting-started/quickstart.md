<!-- Created by VIRAJ :) -->

<!-- My First Three.js Programme. Made with love by Shobhit :) -->
<!DOCTYPE html> 
<html>     
     <head>         
          <meta name="viewport" content="width=device-width, initial-scale=1">
          <meta http-equiv="X-UA-Compatible" content="ie=edge">
          <meta charset="UTF-8">        
          <title>My First Three.js Programme</title>         
          <style>                    
          @import url('https://fonts.googleapis.com/css2?family=Laila&display=swap');        
          body{                                  
          margin:0;                                             
          padding:0;                                                
          scroll-behavior: smooth;                                                
          font-family: 'Laila', sans-serif;                                                
          }       
          h6{                                                
          background-color:#F5F5F5;                                                
          color:#040404;                                                
          padding:2%;                                                
          margin:0;                                                        
          font-size:2rem;                                         
          }                         
          @media screen and (max-width: 600px){         
           h6{                                                                                      
           font-size:0.65rem;
           } 
          }       
          </style>     
    </head>     
    <body>         
         <script src="https://threejs.org/build/three.js"></script>     
         <center>    
         <h6>viraj :)</h6>             
         </center>             
         <script>             
const scene = new THREE.Scene();             
const camera = new THREE.PerspectiveCamera(100, window.innerWidth/window.innerHeight, 1, 10000);             
const renderer = new THREE.WebGLRenderer();             
renderer.setSize(window.innerWidth, window.innerHeight);                                                             
document.body.appendChild(renderer.domElement);                                                     
const geometry = new THREE.BoxGeometry(700, 700, 700, 5, 5, 5);             
const material = new THREE.MeshBasicMaterial({color: 0xffe400,wireframe:true});             
const cube = new THREE.Mesh(geometry, material);             
scene.add(cube);             
camera.position.z = 1200;             
const animate = function(){             
requestAnimationFrame(animate);                 
cube.rotation.x += 0.005;                 
cube.rotation.y += 0.005; 
cube.rotation.z += 0.03;                
renderer.render(scene, camera);             
};             
animate();         
          </script>     
    </body> 
</html>
