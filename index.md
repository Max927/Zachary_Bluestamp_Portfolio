# PyPortal Air Quality Display
My original project was the air quality display on the pyportal, but on top of that I decided to add another project, a weather station that displays the tempurature and the weather conditions in a certain city.  To integrate the two together I utilyzed the pyportal's touchscreen functionality to make an interface that switches between the two.  Over the course of the project I made many mistakes and learned a ton, but if I had to pick one take away from this experience, it would be that I need to slow down sometimes and look around before assuming the worst.
You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Zachary M. | Willow Glen High School | Electrical Engineering | Incoming Senior

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**


For my final milestone I worked on the touchscreen interface to integrate the two projects with one another.  Originally I was going to try to use the "Making a PyPortal User Interface with DisplayIO" project to display the two projects.  I thought it would work since the example of this project had 3 different screens with different displays on them, and I thought that I would be able to just make two of the screens the displays from the first two projects.  However, when trying to figure out the code, there were several issues, first of all several parts of the code were trying to access the wifi at the same time and the pyportal couldn't handle that.  Another issue was when I would try to run the display with the air quality code in it, the actual touchscreen wouldn't function at all, which I still have no idea why that was the case.  So eventually, I scrapped using that code as the base and tried to find another way to switch screens.  Then I found the PyBadger event badge code, which switches between 3 screens when you tap the pyportal anywhere.  I wanted to try this out, so I used it as a base and imported the code from both the weather and air quality projects.  The way the code works is that there are 3 displays and by touching the screen, the display flips between them.  Originally the 2nd and 3rd displays were for your name and email address, but I used code that constructs a URL with the necessary parameters and sends a GET request to the respective API for each project. It then extracts the data, being the AQI, tempurature and weather conditions, from the JSON response and displays it on the badge in each respective display.









# Second Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/PbvK0-TP87c?si=uLyuyqo_LxeEn3MT" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

For my second milestone I decided to add another project on top of my baseline air quality display.  The project I decided to add was the weather station from adafruit since I thought it went hand in hand with the air quality display.  The weather station was much easier to setup than the first project since I already had the libraries installed from the air quality display, I had one error which was quickly resovled when I realized I was missing a library nessecary for the code to run.  For the setup I simply took the example code from the adafruit website walkthrough and put it in my code.py file then imported the one additional library into the lib folder on top of the files from the air quality display.  Also halfway through this milestone I recieved the pieces for the case for my pyportal.  The case was relatively easy to assemble since there was only three pieces.  The first step was to put the back cover over the exposed circuit board on the pyportal, then there was a bracket that screwed into the back cover to keep the pyportal in place.  Finally there was a front cover that snapped into place finishing the case.  In my next milestone I plan to use the touchscreen functionality on the pyportal display in order to make an interface that allows a user to switch between the two projects by touching the screen.  

# First Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/5C1-feZRntU?si=YvZGG8rAJ5RYRKii" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

For my first milestone I made certain the air quality display on the PyPortal was working.  The first step in this was to connect the PyPortal to my computer and download all of the correct libraries into the CIRCUITPY file on my computer.  The next step was for me to connect the PyPortal display to my wifi by using the example code on the adafruit website.  This was the first issue I had since the PyPortal was displaying "AttributeError: 'dict' object has no attribute 'ssid'" , it turns out there was another library that was nessecary to the project that was not shown on the website.  The issue was that I was missing that library.  Finally, I had to input the zip code for my area and the air quality should be displayed.  The issue was that the PyPortal was not showing anything on it's screen and the serial console was displaying "Reply is OK! Response is -1" which is not a valid number for air quality.  The fix to this problem was a little easier, because it turns out my zipcode did not have data from the Air Quality Index used by the code from adafruit, so I changed the zipcode to the nearest one with data.  My plan for the future is to incorporate additional code to change the display and to assemble a magnetic case for the pyportal.


# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

}
```

# Bill of Materials
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Pyportal | Display Screen for Project | $54.95 | https://www.adafruit.com/product/4116 |
| Power Supply | To Provide Power to PyPortal | $7.95 | https://www.adafruit.com/product/1994 |
| MicroUSB Cable | To Connect PyPortal to Computer | $2.95 |  https://www.adafruit.com/product/592 |
| Micro SD Card | Extra Storage | $19.99 |  https://www.adafruit.com/product/2693 |
| Black Nylon Machine Screw and Stand-off Set – M2.5 Thread | For Screwing the Case Together | $16.95 |  https://www.adafruit.com/product/3299 |
| Pyportal 3d Printed Case | Extra Storage | $19.99 |  https://www.adafruit.com/product/2693 |

# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
