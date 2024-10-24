# Cloning a beautiful website layout with html and css

## The Site
#### www.bairlymedia.com

I decided on cloning this site because the layout caught my eye.  The landing page is dynamic with a mixture of videos, photographs, and animation.  As you scroll down, each page section highlights an important part of the owner's wedding photography and videography business.  The sections flow together well, but have distinct styling.

### Working Session 1

#### Getting Started
I set up my new repository starting in VSCode with creating a new project folder and initializing it as a github repository.  I then added my html and css boilerplates.  Adding the basic html architecture included adding a \<header> with two \<nav> elements, a \<main> with two \<section> elements (one for above the fold and one for the rest of the site), and a footer.

#### Above the fold background image styling
The original site's above the fold section fades in nicely.  It's background starts as a video with a dark background so the white title and text on the screen is easy to read.  The background then switches between photos, sets of photos, and other videos to keep interest.  There is a gray overlay to help the white text stand out.

<img width="1500" alt="Screenshot of bairlymedia.com website" src="https://github.com/user-attachments/assets/2681b61e-be18-4dcf-a3df-53ae11aeceb0">


I started with a single background photograph and spent a lot of time fiddling around with the css properties background-origin, background-size, and background-position to enlarge my couple and shift them to the left of the screen.  Instead of a simple gray overlay, I added a gradient that is darker on the left, where my title is and lighter on the right where my couples' faces are.  It also took me time to work out the fade-in animation, having it start as a black screen and fading in the photo and gradient.

<img width="1500" alt="Screenshot of background image with title" src="https://github.com/user-attachments/assets/4a894c42-504e-44eb-91f0-19c306e8d1ee">


### Working Session 2
#### Navigation
The top navigation was straight forward for me using flexbox, but I had to fiddle with the social media navigation's rotation and placement.  I also needed to add position to each to create a stacking context so I could give them each a z-index of 1 so they appear above the background image.

<img width="1500" alt="Screenshot with added navigation menus" src="https://github.com/user-attachments/assets/02fab13b-9e24-4a40-a949-a14c2e2e1758">


### Working Session 3
#### Correcting the hero section
Adding content to sections below my above the fold, hero section showed that my solutions for styling the image relied on it being the only section in the site.  I had to change the positioning on the section.  I originally used `position: fixed; top: 0;` to start it at the top of the document, but then it is taken out of document flow and doesn't scroll up.  Switching to `position: relative; top: -67px;` keeps it in the document flow and moves it up the height of the top nav.  I avoided that solution at first because I didn't want to code an exact number.

Now my section can scroll up out of the way, but I have my background-image set as fixed as well, so it doesn't scroll up as desired.  Removing `background-attachment: fixed;` resolves this isssue.

To have my screen start black, then have the hero section fade in, I added `background-color: black;` to the body element.  I really only want my hero section to start as black, so I added a #hero-container around it and set it's background black.  The header then showed with a white background, but moving the positioning information from #hero up into #hero-container makes the entire screen start black.

I added the animation property to each nav menu as well.  Now the hero section works as expected.



