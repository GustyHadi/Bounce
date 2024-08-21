const dvd = document.getElementById('dvd');
const gameArea = document.getElementById('gameArea');

let x = 0;
let y = 0;
let dx = 2;
let dy = 2;
const dvdWidth = dvd.clientWidth;
const dvdHeight = dvd.clientHeight;
const gameWidth = gameArea.clientWidth;
const gameHeight = gameArea.clientHeight;

// Function to generate a random color
function getRandomColor() {
    const letters = '0123456789ABCDEF';
    let color = '#';
    for (let i = 0; i < 6; i++) {
        color += letters[Math.floor(Math.random() * 16)];
    }
    return color;
}

function updateDvdPosition() {
    x += dx;
    y += dy;

    // Bounce off the walls and change color
    if (x <= 0 || x + dvdWidth >= gameWidth) {
        dx = -dx;
        dvd.style.color = getRandomColor(); // Change color on horizontal bounce
    }
    if (y <= 0 || y + dvdHeight >= gameHeight) {
        dy = -dy;
        dvd.style.color = getRandomColor(); // Change color on vertical bounce
    }

    // Update the position of the "DVD" text
    dvd.style.left = x + 'px';
    dvd.style.top = y + 'px';
}

function gameLoop() {
    updateDvdPosition();
    requestAnimationFrame(gameLoop);
}

// Start the game loop
gameLoop();
