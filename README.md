# FINEARTS205
## workshop 0

objective: 
Keep code as simplified and short as possible
To keep code in the save, but not have it working use: control /

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

