# FINEARTS205
## workshop 0

objective: 
Keep code as simplified and short as possible

Using the p5.js primitive shapes, I experimented with the square and worked on changing the colour, changing the background, getting it to move and getting it to follow the mouse. Having 0 experience coding, I was able to see that this wasn’t as daunting as I expected. This is the code I used to create the shape, colour it, and have it follow my mouse. 


let x = 0 ;

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(100, 100, 10);
  
//   fill(150, 0, 100);
//   rect(mouseX, mouseY, 40, 60)
  
//   x= x + 3


}

I wanted to keep my variables simple and similar to the workshop as I have no experience with coding, so wanted to ease myself into it. Keeping the variable to just the simple X, giving it the initial value of 0, I am able to set up a changabe and adaptable code that I am able to edit if I need to in the future. My code did not contain any conditional formatting yet, so I made sure to practice working with these to  add in a ‘let’ or ‘if’ statement. My code turned into:

let x = 0;

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(100, 100, 10);

  fill(150, 0, 100);
  rect(mouseX, mouseY, 40, 60);
  
  x = x + 3; // x increases by 3 each frame
}

Current code: https://editor.p5js.org/melisssa/full/DW77RT8X7 


## workshop 1
Current code: https://editor.p5js.org/melisssa/full/3EK7JGzph 

Definition Learnt: Local variables are codes that can only be used inside the function.

In this workshop I wanted to try to have shapes generated randomly and move each time so I took inspiration from the workshop and had my code resemble gold stars on a twilight blue sky. I had a lot of trouble finding the way to create a star shape, and was unable to find a star shape that I liked in the P5.js database, so instead I chose to just make the stars round circles as they resembled the stars better than some of the other prism like shapes on the shape library. I also did not want an outline on my shapes so I made sure to use the noStroke () option. 


I probably would have been able to shorten my code by taking out all of the: let x+= let Y= lines, by turning them into one of the lines of code shown in the workshop. But I could not find a way to do this without P5.js coming up with a syntax error. 
![Screen Shot 2025-01-09 at 7 47 44 PM](https://github.com/user-attachments/assets/64863d0d-9777-4fa9-be45-bdba2ed02cba)


I will need to work on this in my next workshop task. 



## workshop 2
Current sketch: https://editor.p5js.org/melisssa/full/jTs0vLPzH 

Objective: To have things showing up on screen after the mouse is pressed/ to use the setTimeout and setInterval functions. 


In this code, since I am very new to coding, I wanted to make sure I was able to understand what each bit of code was for, so that I do not get confused with all the unfamiliar script on the screen; to familiarise myself with the functions of the code I made notes next to the different parts of the code, this was also done in preparation for our tasks next week. 
Again, sticking to the star in the night looking sketch I didn’t want to start my code from scratch, so instead I tried to incorporate the etTimeout and setInterval functions into my pre-existing code. To do this I followed the given structure, and adapted it to the pre-existing code, making sure to leave notes in the code as I went along, so that I did not confuse myself. I decided to keep the interval time of 1000ms (one second) so that the stars looked like they were twinkling. If I wanted to make the stars a little slower in repopulating, I could have raised the interval time, but I was happy with where it was at. I think there is probably a way to shorten the code a little bit, as I think the amount of lines I have is a little but too much for the simplistic nature of the sketch, so my focus going into my next sketch would be to try and make the code simpler. I think because I am so new to coding that this will come with time and as I gain more experience. 

Current code:

let counter = 0;
let countInterval;
function setup() {
  createCanvas(400, 400);
  noStroke();
  background(0, 0, 120); // Set background to dark blue
  let numStars = 100; // Number of stars to create

  for (let i = 0; i < numStars; i++) {
    let x = random(width);
    let y = random(height);
    let size = random(3, 8); // Random sizes for each star
    drawStar(x, y, size);
  }
  // Start the timed interval to draw more stars at a regular interval
  countInterval = setInterval(makeStar, 1000); // Make a star every second
}

// Function to draw a star
function drawStar(x, y, size) {
  fill(255, 223, 0); // Gold color
  ellipse(x, y, size, size); // Draw a circle for the star
}
// Function to draw a new star at a random location
function makeStar() {
  let x = random(width);
  let y = random(height);
  let size = random(3, 8);
  drawStar(x, y, size);

  
 
  counter++; // Increment the counter after drawing a star
  if (counter >= 5) { // Stop after 5 stars are drawn
    clearInterval(countInterval);
    counter = 0; // Reset counter
  }
}
// Added a mouse pad function as well, so that when mouse is pressed, the randomised background will reset to another random spacing
function mousePressed() {
  counter = 0;
  background(0, 0, 120); // Reset background to dark blue
  for (let i = 0; i < 100; i++) { // Redraw the initial set of stars
    let x = random(width);
    let y = random(height);
    let size = random(3, 8);
    drawStar(x, y, size);
  }
  // Restart the interval to draw stars like in the workshop example
  countInterval = setInterval(makeStar, 1000);
}


