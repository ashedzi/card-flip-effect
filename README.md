# Card Flip Animation with CSS: A Simple Tutorial for Beginners

Have you ever been scrolling through a website and come across an impressive card flip animation, 
wondering how it was done? In this tutorial, we'll walk through how to create a fun and interactive 
card flip animation using just HTML and CSS. It's a cool effect that you can add to your projects 
to impress visitors. No complex JavaScript required!

## What You'll Learn
- How to create a simple card flip animation with CSS.
- How to use CSS properties like transform, perspective, and backface-visibility to achieve this effect.

## Step 1: Setting Up Your HTML Structure
First, we'll create the basic HTML structure. This will include a container for the card and two sides 
(front and back) for each card. Here's the code to get started
```html 
           <main>
            <div class="card-container flex gap-20">
                <figure class="me">
                    <img src="./assets/img/waving.png">
                </figure>
                <div class="card">
                    <div class="front grid">
                        <h2>Hover to reveal secret</h2>
                    </div>
                    <div class="back grid">
                        <figure>
                            <img src="./assets/img/hi.png">
                        </figure>
                        <p>Hey there! I'm Ashedzi a software developer, nice to meet you.</p>
                    </div>
                </div>
            </div>
        </main>
```
**Explanation:**
- We have a card-container to hold the cards.
- Each card has a front and back side.
- We use flex and grid to center the content and add spacing between cards.

## Step 2: Applying CSS for the Card Flip Effect
### Key CSS Features for the Flip Effect
- Perspective
```css
    .card-container {
    height: 100dvh;
    perspective: 1000px;
}
```
**Explanation:** 
perspective gives a 3D effect. It controls how far the viewer is from the card, making the flip look more realistic.

### Positioning and Transforming the Card
```css
.card, .card2 {
    position: relative;
    width: 200px;
    height: 300px;
    transform-style: preserve-3d;
    transition: transform 0.6s;
    border-radius: 5px;

    &:hover {
        transform: rotateY(180deg);
    }
}

```
**Explanation:** 
- transform-style: preserve-3d keeps the 3D effect intact, and transform: rotateY(180deg) rotates the card 
when hovered to create the flip.

### Positioning Front and Back

```css 
    .front, .back {
        position: absolute;
        width: 100%;
        height: 100%;
        border-radius: 5px;
        backface-visibility: hidden;
    }
```
**Explanation:** 
- position: absolute stacks the front and back on top of each other.
- backface-visibility: hidden ensures the back side is hidden when flipped.


### Flipping the Back
```css
    .back {
        color: #fff;
        transform: rotateY(180deg);
        text-align: center;
    }
```
**Explanation:** 
- Initially, the back side is rotated by 180 degrees to keep it hidden. When hovered, 
both sides flip, showing the back.

**Check out my full code to see how these features were all merged together to get the perfect design**

## Conclusion
That's it! You've successfully created a simple and fun card flip animation using just HTML and CSS. 
This is a great effect to add interactivity to your website with minimal code.

Feel free to check out my code and customize your card’s content and appearance by adjusting the text, images, 
and colors. Happy coding!
