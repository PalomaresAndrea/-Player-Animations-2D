# 🎮 Tutorial de Unity – Patrones de Software y Animaciones

## 📌 Objetivo
- ★ Hablaremos del diseño de patrones de software utilizados en Unity.  
- ★ Crear animaciones para un jugador.  

---

## 🛠️ Procedimiento

1. **Crear un nuevo proyecto en Unity Hub**  
   - Seleccionar la versión más actual disponible.  
   - En el cuadro de diálogo, elegir la opción **2D RPG**.  
   - Asignar un nombre al proyecto (ejemplo: `RPG`) y una ruta de almacenamiento.  
   - Presionar **CREATE** y esperar la inicialización.  
<img width="1098" height="66" alt="image" src="https://github.com/user-attachments/assets/cc68f49b-9ac3-4b8b-a5ee-d5aec27bbef8" />

2. **Configurar la estructura del proyecto**  
   - Crear la carpeta de directorios según la imagen de referencia.
     <img width="480" height="397" alt="image" src="https://github.com/user-attachments/assets/d6122399-43fd-4442-b2f0-6c6cb8da810e" />

   - Abrir Unity IDE y crear **dos objetos vacíos** en la vista *Hierarchy*:  
     - `PlayerObject`  
     - `EnemyObject`
       <img width="427" height="238" alt="image" src="https://github.com/user-attachments/assets/691d3575-0c6c-4566-a3db-258c783aeaac" />


3. **Agregar componentes principales**  
   - Seleccionar `PlayerObject` → *Add Component* → **Sprite Renderer**.  
   - Repetir el proceso para `EnemyObject`.
   <img width="1037" height="1473" alt="image" src="https://github.com/user-attachments/assets/b25f147c-9649-456a-a26f-3be0f9e9ca3d" />

   - Guardar la escena como **LevelOne** en la carpeta `Scenes`.
  <img width="1098" height="46" alt="image" src="https://github.com/user-attachments/assets/d834f5dc-6ef0-4304-80d9-543b40e5703a" />

     

4. **Importar recursos gráficos**  
   - Descargar los archivos de sprites:  
     - `Player.png`  
     - `EnemyIdle_1.png`  
     - `EnemyWalk_1.png`
   <img width="1098" height="310" alt="image" src="https://github.com/user-attachments/assets/c9f42aa5-0823-4bed-b600-5303359c7f34" />

   - Arrastrarlos a la carpeta `Sprites`.  
   - Ajustar las propiedades de `Player.png` en el *Inspector* y aplicar cambios.  
<img width="1039" height="1369" alt="image" src="https://github.com/user-attachments/assets/6dd9c650-5957-4e40-9802-1a379dea05d4" />

5. **Dividir sprites con el Sprite Editor**  
   - Ir a `Window → 2D → Sprite Editor`.  
   - Usar la opción **Slice** para separar los sprites individuales.  
   - Confirmar con el botón de la esquina inferior derecha.  
<img width="1025" height="1152" alt="image" src="https://github.com/user-attachments/assets/311ebd4f-5ec1-403e-9305-694edd24a902" />

6. **Asignar sprites a objetos**  
   - En `PlayerObject`, seleccionar un sprite en la propiedad **Sprite**.
     <img width="587" height="124" alt="image" src="https://github.com/user-attachments/assets/605d82fe-cdfa-463f-a4f3-08175828ebbb" />

   - Repetir el proceso con `EnemyIdle_1` y `EnemyWalk_1`.  
<img width="1070" height="1441" alt="image" src="https://github.com/user-attachments/assets/d35c74db-6ed9-4927-a216-de660693966e" />

---

## 🎞️ Animaciones

1. **Crear animaciones para el jugador**  
   - Expandir los sprites de `Player`.  
   - Seleccionar los cuatro primeros y arrastrarlos a `PlayerObject`.
   <img width="1098" height="547" alt="image" src="https://github.com/user-attachments/assets/097c60e4-75f0-481c-9f65-1531c064dadf" />

   - Guardar la animación como `player-walk-east` en la carpeta `Animations`.
     <img width="1098" height="839" alt="image" src="https://github.com/user-attachments/assets/400eecd7-fb3a-4fe9-9b9c-4b60ce3342ef" />

2. **Configurar Animator**  
   - Observar que ahora `PlayerObject` tiene:  
     - `Sprite Renderer`  
     - `Animator` con un `Animator Controller`.  
   - Renombrar el controller a **PlayerController** y moverlo a `Animations/Controllers`.
   <img width="1098" height="617" alt="image" src="https://github.com/user-attachments/assets/ab5aaad1-629e-4d6d-bf9a-c47f001243fd" />

   - Abrirlo con doble clic para acceder a la ventana *Animator*.  
<img width="1098" height="617" alt="image" src="https://github.com/user-attachments/assets/af963fdf-0df2-4ade-9a31-a7db7a9f479c" />

3. **Agregar el resto de animaciones**  
   - `player-walk-west`  
   - `player-walk-south`  
   - `player-walk-north`  
   - `player-idle`  
<img width="1098" height="617" alt="image" src="https://github.com/user-attachments/assets/1232e037-86a2-4113-8fc4-63d3fd8d1ad9" />
<img width="786" height="647" alt="image" src="https://github.com/user-attachments/assets/c9a1f975-845c-4eeb-b0d8-a24a7187018f" />
<img width="1098" height="617" alt="image" src="https://github.com/user-attachments/assets/0d36d3be-a8d2-4f36-b5b4-5773465c20f8" />

4. **Configurar la cámara y probar**  
   - Seleccionar `Main Camera` → cambiar propiedad **Size = 1**.  
   - Presionar **Play**.  
<img width="1098" height="617" alt="image" src="https://github.com/user-attachments/assets/78e28629-a370-46a0-9ba0-be02273ee84e" />

5. **Ajustar velocidad de animación**  
   - Abrir la ventana *Animator*.  
   - Seleccionar `player-walk-east` y cambiar **Speed = 0.6**.  
<img width="1003" height="1102" alt="image" src="https://github.com/user-attachments/assets/cb02791f-7bab-404b-b87f-074bfe4a5e9e" />

---

## 🎯 Desafío

- Crear y guardar las animaciones para `EnemyWalk_1` y `EnemyIdle_1`.
  - Cada animación contiene 5 sprites.  
- Nombrar:  
  - `enemy-walk-1`  
  - `enemy-idle-1`  
- Renombrar `EnemyObject Animation Controller` a **EnemyController** y moverlo a `Animations/Controllers`.  
- Mover las animaciones enemigas a `Animations/Animaciones`.  
<img width="1098" height="83" alt="image" src="https://github.com/user-attachments/assets/65f3ec06-5397-4cf0-b856-5af001727363" />
<img width="1098" height="834" alt="image" src="https://github.com/user-attachments/assets/92b713ec-fed5-456d-b76f-53f02e3070bc" />
<img width="1098" height="619" alt="image" src="https://github.com/user-attachments/assets/ab61f1df-d1ae-4b3b-b870-ce5101f4a85e" />

