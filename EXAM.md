### 1. Get DOM elements using Javascript selectors

* Select an __IMG__ element
* var images = document.querySelector("img");
* Select all __H2__ elements
* var H2 = document.querySelectorAll("h2");
* Select all __A__ elements that have the attribute _title_
* var A = document.querySelectorAll("a[title]");
* Select only the __IMG__ elements that are inside an __A__ element
* var imgInA = document.querySelectorAll("a > img");
* Select all elements with class _article_
* var article = document.querySelectorAll("article");
* Select all _article_ from the middle and right column, but not from the left column
* //I tried to select the articles of the section opening-1-right but it doesn't seams to work.
 var noLeft = document.querySelectorAll('section[class*=”right”] > article ');
* Select the 4th and 5th _article_ from the left column
* eftArticle = document.getElementsByClassName('opening-1-left')[0]; 
leftArticle.childNodes[0].childNodes[3];
leftArticle.childNodes[0].childNodes[4];
* Select the logo of the website
* var logo = document.querySelector("a[href='/']");
* Select all __IMG__ elements whose _SRC_ attribute is a _JPG_ file
document.querySelectorAll('img[src$=".jpg"]');
### 2. Apply CSS to DOM

* Change the main article title to FF0000
* document.getElementsByClassName('fs-66')[0].childNodes[0].textContent = "FF0000";
* Change page background color to green
* document.getElementsByTagName('body')[0].setAttribute('style','background-color:green;'); 
* Change subtitles to lowercase
* //I don't know what do you mean by subtitle I supouse you are refering to the second title so I defined that a subtitle is what has h3 tag.
x = document.querySelectorAll("h3"); 
var i; for (i = 0; i < x.length; i++) {document.getElementsByTagName("h3")[i].textTransform = "lowercase";  } 
* Hide opinion column
* var opinionColumn = document.getElementsByClassName('opening-1-right-bottom-right')[0]; 
opinionColumn.setAttribute('style','visibility:hidden;');
* Make top Ad banner sticky at the bottom
var addBanner = document.getElementById('1_970x90_1');
addBanner.setAttribute('style', 'position:absolute; bottom:-1200rem');
### 3. DOM Manipulation with Javascript

* Add a 10px red border around all __IMG__ elements 
* img = document.getElementsByTagName('img');
function borderImage(){
	for(i=0;i<img.length;i++){
		img[i].setAttribute('style','border: 10px solid red;');
	};
};
borderImage();
* Fade out all __IMG__ elements
* function fadeOut(el){
	el.style.opacity = 1;
	(function fade() {
		if ((el.style.opacity -= .1) < 0) {
			el.style.display = "none";
		} else {
			requestAnimationFrame(fade);
		}
	})();
};
var img = document.getElementsByTagName('img');

function fadeArray(){
	for(i=0;i<img.length;i++){
		fadeOut(img[i]);
	};
};
fadeArray();
* Add a 10px red border around all __IMG__ and fade out the images after 3 seconds
img = document.getElementsByTagName('img');
function borderImage(){ 
	for(i=0;i<img.length;i++){
		img[i].setAttribute('style','border: 10px solid red;');
	};
};
borderImage();
function fadeOut(el){
	el.style.opacity = 1;
	(function fade() {
		if ((el.style.opacity -= .1) < 0) {
			el.style.display = "none";
		} else {
			requestAnimationFrame(fade);
		}
	})();
};
var img = document.getElementsByTagName('img');
function fadeArray(){
	for(i=0;i<img.length;i++){
		fadeOut(img[i]);
	};
};
setTimeout(function(){  
    fadeArray(); 
},3000);

### 4. Answer the following points

* Justify the chosen method used to hide opinion column
I used the method hidde because if I removed it the other columns would be afected and they will be moved and the page would look worst.
* Explain the difference between position static, relative, absolute and fixed
Static: Default value. Elements render in order, as they appear in the document flow relative: The element is positioned relative to its normal position, so "left:20" adds 20 pixels to the element's LEFT position.
Absolute: The element is positioned relative to its first positioned (not static) ancestor element.
Fixed: The element is positioned relative to the browser window.

* What are data SRCs? When would you use them?
SRC is used to tell to the browser the source of the file, it can be used for images, sounds, scripts, etc.
* What benefits you get by using a CSS preprocessor?
It makes the code more modular, reduce redundanci wich allows to save space and encrease the SEO of the website and you can reuse it for other projects.
* Why would you use unit testing?
Could be very usefull to check if the web page or the app can breack or have some sorts of bugs in it.
* How would you accelerate an element by hardware and why?
I would used to increase the speed of rendering which could be needed for some sorts of CSS animations. It can be also used to make the animation use less computer resources so you don't waste too much RAM.


