import gab.opencv.*;
import java.awt.Rectangle;


Rectangle[] faces;

import gab.opencv.*;
import processing.video.*;
import java.awt.*;

Capture video;
OpenCV opencv;

void setup() {
  size(640, 480);
  video = new Capture(this, 640/2, 480/2);
  opencv = new OpenCV(this, 640/2, 480/2);
  opencv.loadCascade(OpenCV.CASCADE_FRONTALFACE);  

  video.start();
}

void draw() {
  scale(2);
  opencv.loadImage(video);

  image(video, 0, 0 );

  noFill();
  stroke(0, 255, 0);
  strokeWeight(3);
  Rectangle[] faces = opencv.detect();
  println(faces.length);
  
  
int colorVal=0;


if (keyPressed){
    if (key == 'a'){
      
for (int i = 0; i < faces.length; i++) {
    println(faces[i].x + "," + faces[i].y);
    rect(faces[i].x, faces[i].y, faces[i].width, faces[i].height);
    stroke(colorVal);
    rect(faces[i].x+15, faces[i].y+25, faces[i].width/4, faces[i].height/4);
    rect(faces[i].x+50, faces[i].y+25, faces[i].width/4, faces[i].height/4);
    stroke(255,255,255);
    rect(faces[i].x+20, faces[i].y+60, faces[i].width/4+25, faces[i].height/4);

  }
   
  }
      
    }
    else{
      
    }
}
    
  


void captureEvent(Capture c) {
  c.read();
}

//Cite Sources:https://github.com/kylemcdonald/AppropriatingNewTechnologies/wiki/Week-2
