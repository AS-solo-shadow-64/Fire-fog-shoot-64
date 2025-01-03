<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>3D Shooting Game (Mobile)</title>
  <style>
    body {
      margin: 0;
      overflow: hidden;
      font-family: Arial, sans-serif;
    }
    canvas {
      display: block;
    }
    #health {
      position: absolute;
      top: 10px;
      left: 10px;
      color: white;
      font-size: 18px;
      z-index: 1;
    }
    #joystick {
      position: absolute;
      bottom: 20px;
      left: 20px;
      width: 100px;
      height: 100px;
      background: rgba(255, 255, 255, 0.3);
      border-radius: 50%;
      z-index: 2;
      touch-action: none;
    }
    #shootButton {
      position: absolute;
      bottom: 30px;
      right: 20px;
      width: 80px;
      height: 80px;
      background: rgba(255, 0, 0, 0.5);
      border-radius: 50%;
      z-index: 2;
      touch-action: none;
    }
  </style>
</head>
<body>
  <div id="health">Health: 100</div>
  <div id="joystick"></div>
  <div id="shootButton"></div>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
  <script>
    // Scene setup
    const scene = new THREE.Scene();
    const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
    const renderer = new THREE.WebGLRenderer();
    renderer.setSize(window.innerWidth, window.innerHeight);
    document.body.appendChild(renderer.domElement);

    // Lighting
    const light = new THREE.DirectionalLight(0xffffff, 1);
    light.position.set(10, 20, 10).normalize();
    scene.add(light);

    // Ground
    const groundGeometry = new THREE.PlaneGeometry(50, 50);
    const groundMaterial = new THREE.MeshBasicMaterial({ color: 0xdeb887 });
    const ground = new THREE.Mesh(groundGeometry, groundMaterial);
    ground.rotation.x = -Math.PI / 2;
    scene.add(ground);

    // Player
    const playerGeometry = new THREE.BoxGeometry(1, 2, 1);
    const playerMaterial = new THREE.MeshBasicMaterial({ color: 0x0000ff });
    const player = new THREE.Mesh(playerGeometry, playerMaterial);
    player.position.y = 1;
    scene.add(player);
    camera.position.set(0, 2, 8);
    camera.lookAt(player.position);

    // Enemies
    const enemies = [];
    for (let i = 0; i < 4; i++) {
      const enemyGeometry = new THREE.BoxGeometry(1, 2, 1);
      const enemyMaterial = new THREE.MeshBasicMaterial({ color: 0xff0000 });
      const enemy = new THREE.Mesh(enemyGeometry, enemyMaterial);
      enemy.position.set(Math.random() * 20 - 10, 1, Math.random() * -20);
      enemies.push(enemy);
      scene.add(enemy);
    }

    // Movement variables
    let moveX = 0, moveZ = 0;

    // Joystick control
    const joystick = document.getElementById('joystick');
    let isMoving = false;
    joystick.addEventListener('touchstart', (e) => {
      isMoving = true;
    });
    joystick.addEventListener('touchmove', (e) => {
      const touch = e.touches[0];
      const rect = joystick.getBoundingClientRect();
      const x = touch.clientX - rect.left - rect.width / 2;
      const y = touch.clientY - rect.top - rect.height / 2;
      moveX = x / 50; // Adjust sensitivity
      moveZ = -y / 50;
    });
    joystick.addEventListener('touchend', () => {
      isMoving = false;
      moveX = 0;
      moveZ = 0;
    });

    // Shooting button
    const shootButton = document.getElementById('shootButton');
    shootButton.addEventListener('touchstart', shoot);

    // Shooting logic
    function shoot() {
      enemies.forEach((enemy, index) => {
        const distance = player.position.distanceTo(enemy.position);
        if (distance < 5) {
          enemy.material.color.set(0x808080); // Hit
          scene.remove(enemy); // Remove enemy
        }
      });
    }

    // Game loop
    function animate() {
      requestAnimationFrame(animate);
      if (isMoving) {
        player.position.x += moveX * 0.1;
        player.position.z += moveZ * 0.1;
      }
      renderer.render(scene, camera);
    }
    animate();
  </script>
</body>
</html>
