# Joset
Juegos const canvas = document.getElementById('myCanvas');
const ctx = canvas.getContext('2d');

// Variables para los animales
let animal1 = {
    x: 100,
    y: 100,
    width: 50,
    height: 50,
    color: 'blue'
};

// Función para dibujar el animal
function dibujarAnimal(animal) {
    ctx.fillStyle = animal.color;
    ctx.fillRect(animal.x, animal.y, animal.width, animal.height);
}

// Función para actualizar la posición del animal
function actualizar() {
    // Lógica para actualizar la posición del animal
    animal1.x += 1;
}

// Bucle de animación
function juego() {
    actualizar();
    dibujarAnimal(animal1);
    requestAnimationFrame(juego);
}

juego();

