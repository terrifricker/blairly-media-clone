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

<img width="1708" alt="Screenshot of current state of my website clone" src="https://github.com/user-attachments/assets/4a894c42-504e-44eb-91f0-19c306e8d1ee">


