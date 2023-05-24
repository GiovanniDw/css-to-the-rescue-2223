# 􀢅 CSS To The Rescue

### Assignment
+ **Leerdoelen**
   - Je kunt experimenteren met (voor jou) **nieuwe css-technieken** - om de mogelijkheden op waarde te schatten en te gebruiken waar gepast.
   - Je hebt begrip van de volle kracht en mogelijkheden van CSS. Je laat zien dat CSS meer kan dan allen web pages 'stylen'.
   - Je hebt begrip van de interactie-technieken van CSS (en HTML). De UX is aangenaam bruikbaar binnen de gekozen context(en).
   - Je hebt begrip hoe progressive enhancement elegant toe te passen. Je laat zien dat je cascade, inheritance en specificity kunt toepassen.
+ Rubic
   - [x] Je hebt **geëxperimenteerd** met voor jou nieuwe CSS-technieken.
   - [ ] Je resultaat is een experimentele én aangename ervaring waarbij **inhoud, vorm en interactie** één geheel vormen.
   - [ ] Je laat zien dat je de **mogelijkheden en kracht van CSS begrijpt.** In je code gebruik je CSS, HTML waar ze in uitblinken en combineer je de technieken zodat ze elkaar versterken.
   - [ ] Je code bestaat uit **vanilla CSS** en HTML. Geen JS, pre-processors, libraries en frameworks en alleen ID’s en classes indien strikt noodzakelijk.
   - [ ] **Proces:**
      - [ ] Je website staat tijdig online (op GitHub en DLO) en is zonder technische problemen te zien. Verwijzingen naar bestanden (css, js, afbeeldingen, fonts, etc.) werken. Je website werkt in minimaal één browser naar keuze.
      - [ ] Je code is verzorgd en leesbaar. Netjes ingesprongen, van commentaar voorzien, etc.
      - [ ] Je vermeldt gebruikte bronnen in je code en procesverslag.
      - [ ] Je hebt je vorderingen besproken en je proces vastgelegd en tijdig ontsloten op GitHub.
   - [ ] Je kunt je **code uitleggen** in het eindgesprek.

# Process

### Mijn plan

De CSS technieken waar ik mee ben begonnen;

- `animation`
- `@keyframes`
- `transforms`
- `background-position`
- `font-variable`
- `@media preferes-color-scheme`

![Image.png](README.assets/Image.png)

![Image.png](README.assets/Image%20(2).png)

```javascript
h1 {
  font-size: 5vw;
  font-variation-settings: 'XROT' 30, 'YROT' 30;
  background-size: auto auto;
  background-clip: border-box;
  background-size: 200% auto;
  background-clip: text;
  text-fill-color: transparent;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: FontVars 10s infinite linear both;
  transform: translateZ(-1px) scale(2.2);
}
```

![Image.png](README.assets/Image%20(3).png)

```javascript
@media (prefers-reduced-motion: reduce) {
  h1 {
    animation: FontVars 5s infinite linear both;
  }
}

@media (prefers-color-scheme: dark) {
  h1 {
    background-image: radial-gradient(circle,
        #231557 0%,
        #44107a 29%,
        #ff1361 67%,
        #fff800 100%);
    animation: textclip 2s linear infinite;
  }
}

@keyframes textclip {
  to {
    background-position: 200% center;
  }
}

@keyframes FontVars {
  0% {
    font-variation-settings: 'XROT' -40, 'YROT' 1;
	}
  25% {
    font-variation-settings: 'XROT' 10, 'YROT' -40;
	}
  50% {
    font-variation-settings: 'XROT' 40, 'YROT' 40;
	}
  75% {
    font-variation-settings: 'XROT' 10, 'YROT' -40;
	}
  100% {
    font-variation-settings: 'XROT' -40, 'YROT' 1;
	}
}
```

![Screenshot 2023-04-20 at 18.39.21.png](README.assets/Screenshot%202023-04-20%20at%2018.39.21.png)

### Voortgang

#### `@media (prefers-color-scheme)`

![Screenshot 2023-04-20 at 17.33.39.png](README.assets/Screenshot%202023-04-20%20at%2017.33.39.png)

![Screenshot 2023-04-20 at 17.34.18.png](README.assets/Screenshot%202023-04-20%20at%2017.34.18.png)

#### `@media (width < width)`

![Image.png](README.assets/Image%20(4).png)

![Screenshot 2023-04-20 at 17.33.46.png](README.assets/Screenshot%202023-04-20%20at%2017.33.46.png)

![Screenshot 2023-03-04 at 23.49.49.png](README.assets/Screenshot%202023-03-04%20at%2023.49.49.png)

![Screenshot 2023-03-04 at 23.49.46.png](README.assets/Screenshot%202023-03-04%20at%2023.49.46.png)

Het positioneren van sommmige elementen ging lastig, en was anders in verschillende browsers. Dit is uiteindelijk opgelost door op het parent element ook een positioning te geven

met target selector to scroll geprobeert om parralax elementen toe te voegen, maar dit is helaas niet gelukt.

Feedback

Iets meer beweging, en css

### Afronding

![Screenshot 2023-04-20 at 17.34.40.png](README.assets/Screenshot%202023-04-20%20at%2017.34.40.png)

![Screenshot 2023-04-20 at 17.35.18.png](README.assets/Screenshot%202023-04-20%20at%2017.35.18.png)

#### Interacties

Media Queries

**Css Technieken**

Context

`@media prefers-color-scheme`

**Kleur**

**Animation & Transform**

`@keyframes`

`font-variation-settings`

`@container (width < …)`

`transform: translateY();`

**Layout**

**Selectors**

**Effects**

---

# Bronnen

[CSS-Only Responsive Layout with Smooth Transitions | Codrops](https://tympanus.net/codrops/2012/06/12/css-only-responsive-layout-with-smooth-transitions/)

[Using CSS animations - CSS: Cascading Style Sheets | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations)

[text-color-animation](https://codepen.io/alvarotrigo/pen/PoKMyNO)

[Eindopdracht - CSS to the Rescue 22/23](https://cmda-minor-web.github.io/css-to-the-rescue-2223/index.html#vuurwerkshow)

[Font scaling based on size of container](https://stackoverflow.com/questions/16056591/font-scaling-based-on-size-of-container)

---

### Font Scaling

1814

\+350

If the container is not the body, CSS Tricks covers all of your options in [*Fitting Text to a Container*](https://css-tricks.com/fitting-text-to-a-container/).

If the container is the body, what you are looking for is [Viewport-percentage lengths](http://dev.w3.org/csswg/css-values/#viewport-relative-lengths):

> The **viewport-percentage lengths** are relative to the size of the [initial containing block](https://www.w3.org/TR/CSS21/visudet.html#containing-block-details). When the height or width of the initial containing block is changed, they are scaled accordingly. However, when the value of overflow on the root element is auto, any scroll bars are assumed not to exist.
The values are:

- `vw` (% of the viewport width)
- `vh` (% of the viewport height)
- `vi` (1% of the viewport size in the direction of the root element's inline axis)
- `vb` (1% of the viewport size in the direction of the root element's block axis)
- `vmin` (the smaller of `vw` or `vh`)
- `vmax` (the larger or `vw` or `vh`)

1 v* is equal to 1% of the initial containing block.

Using it looks like this:

```css
p {
    font-size: 4vw;
}
```

As you can see, when the viewport width increases, so do the `font-size`, without needing to use media queries.

These values are a sizing unit, just like `px` or `em`, so they can be used to size other elements as well, such as width, margin, or padding.

Browser support is pretty good, but you'll likely need a fallback, such as:

```css
p {
    font-size: 16px;
    font-size: 4vw;
}
```

Check out the support statistics: [http://caniuse.com/#feat=viewport-units](http://caniuse.com/#feat=viewport-units).

Also, check out CSS-Tricks for a broader look: [*Viewport Sized Typography*](http://css-tricks.com/viewport-sized-typography/)

Here's a nice article about setting minimum/maximum sizes and exercising a bit more control over the sizes: [*Precise control over responsive typography*](http://madebymike.com.au/writing/precise-control-responsive-typography/)

And here's an article about setting your size using calc() so that the text fills the viewport: [http://codepen.io/CrocoDillon/pen/fBJxu](http://codepen.io/CrocoDillon/pen/fBJxu)

Also, please view this article, which uses a technique dubbed 'molten leading' to adjust the line-height as well. [*Molten Leading in CSS*](https://css-tricks.com/molten-leading-css/)

[Taming Advanced CSS Selectors](https://www.smashingmagazine.com/2009/08/taming-advanced-css-selectors/)

