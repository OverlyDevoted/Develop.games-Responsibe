# Develope.games. Responsiveness Update
One innocent day, when I was watching Pirate Software livestream, the stream-master Thor, talked about a compendium for aspiring game devs. So I decided to check the website on my phone for myself as I'm somewhat of an avid game dev... And oh my god, the things I saw... UNRESPONSIVE DESIGN! As an apprentice in front-end magic I decided to dibble and dabble and try to make the website more mobile usable for mobile goblins. I tried to not compromise on the simplicity of the website and the minimal use of javascript and more modern CSS features. With this I hope I can show stream-master Thor that there's another way, a more responsive way...  

## Initial analysis
### User experience from user standpoint
First, I downloaded all the HTML and CSS code, then and all the pictures. I started of with playing around with the webpage size to see how it reacts to different sizes. The element sizes were constant pixel size, so no element scales with the screen size so when you make your screen smaller, the element stay the same size and you have to scroll to navigate the website. After that I checked out the website on my phone and the website was all zoomed out to fit the whole width, which was not readable without zooming and I had to do a lot of manual horizontal scrolling to navigate through the site. 

![Initial mobile view](/assets/readme/initial_mobile.jpg)

## HTML and CSS
After getting an idea of website's responsiveness from user standpoint, I proceeded to examine the website's code. I noticed that it contains very minimal JS, most of JS in use was from Twitch embed and some CloudFare scripts. I found that `<br>` was the main element for spacing elements. Also there was the of use non-existent tag `grid`. 

## Google PageSpeed Insights
I ran all tests on local environment
PageSpeed identified these main issues:
### Performance
1. Images are too large (8.82s)
2. Some images are too large in size (8.05s)
3. There's unused Javascript that takes too long (6.88s)

### Accessibility
1. Image `alt` and HTML `lang` tags 

### Best practices
1. Issues from this category stemmed all from twitch stream scripts so I ignored it

### SEO
1. And some missing meta headers.

## Goals

With this information I set out to make the website more responsive while fixing PageSpeed insight issues along the way. These are the goals I set for myself:
1. Make the main content of the website always in the middle and scale with screen size
2. On smaller screens make toggle with a button
3. Reduce image size and 
4. Make hyperlinks open on a new tab
5. Use as little JS as possible
6. Refactor CSS and HTML to reduce size and increase readability

## Results
- Navbar is now expandable as a sidebar on certain screen sizes.
- External hyperlinks now open a new tab instead of opening a new page on the same tab. 
- Utilize syntactic HTML for improved accessibility 
- Labeled all images
- Reduced image size by about 46.6%. (Funny that scam_splash size got reduced by 94%) 

### Desktop
![Desktop Final](/assets/readme/developGames.gif)
### Mobile
![Mobile Final](/assets/readme/mobile.gif)

## PageSpeed comparison

### Desktop
#### Before
![Before Desktop PageSpeed](/assets/readme/initialDesk.PNG)
#### After
![After Desktop PageSpeed](/assets/readme/resDesk.PNG)

### Mobile
#### Before
![Before Mobile PageSpeed](/assets/readme/initialMobile.PNG)
#### After
![After Mobile PageSpeed](/assets/readme/results.PNG)