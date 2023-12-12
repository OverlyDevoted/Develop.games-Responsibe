# Develope.games. Responsiveness Update
One innocent day, when I was watching Pirate Software livestream, the stream-master Thor, talked about a compendium for aspiring game devs. So I decided to check the website on my phone for myself as I'm somewhat of an avid game dev... And oh my god, the things I saw... UNRESPONSIVE DESIGN! As an apprentice in front-end magic I decided to dibble and dabble and try to make the website more mobile usable for mobile goblins. I tried to not compromise on the simplicity of the website and the minimal use of javascript and more modern CSS features. With this I hope I can show stream-master Thor that there's another way, a more responsive way...  

## Initial analysis
### User experience from user standpoint
First, I downloaded all the HTML and CSS code, then and all the pictures. I started of with playing around with the webpage size to see how it reacts to different sizes. The element sizes were constant pixel size, so no element scales with the screen size so when you make your screen smaller, the element stay the same size and you have to scroll to navigate the website. After that I checked out the website on my phone and the website was all zoomed out to fit the whole width, which was not readable without zooming and I had to do a lot of manual horizontal scrolling to navigate through the site. 

![Initial mobile view](/assets/readme/initial_mobile.jpg)

## HTML and CSS
After getting an idea of website's responsiveness from user standpoint, I proceeded to examine the website's code. I noticed that it contains very minimal JS, most of JS in use was from Twitch embed and some CloudFare scripts. I found that `<br>` was the main element for spacing elements. Also there was the of use non-existent tag `grid`.      

## Google PageSpeed Insights


- Navbar is now expandable as a sidebar on certain screen sizes.
- [ ] Hyperlinks now open a new tab instead of opening a new page on the same tab. 
- [ ] Utilize syntatic HTML for improved accessibility 
- [ ] Optimize images 