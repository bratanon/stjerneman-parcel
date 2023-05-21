```javascript
  <script>
    const element = document.getElementsByClassName('dev').item(0);

    const setScreenSize = () => {
      const screenSize = window.innerWidth;
      element.setAttribute('data-size', screenSize.toString());
    };

    setScreenSize();

    window.addEventListener('resize', setScreenSize);
  </script>
```
```css
body.dev {
  padding-top: 20px;

  &:before {
  height: 20px;
  width: 100%;
  position: fixed;
  top: 0;
  color: #FFF;
  font-weight: bold;
  font-size: 12px;
  text-align: center;

    background-color: red;
    content: 'min - ' attr(data-size);

    @media screen and (min-width: 425px) {
      content: '425 - ' attr(data-size);
      background-color: #9800f3;
    }

    /*@media screen and (min-width: 520px) {*/
    /*  content: '520 - ' attr(data-size);*/
    /*  color: #000;*/
    /*  background-color: #ffff00;*/
    /*}*/

    @media screen and (min-width: 768px) {
      content: '768 - ' attr(data-size);
      background-color: #00b3ee;
    }

    @media screen and (min-width: 960px) {
      content: '960 - ' attr(data-size);
      background-color: green;
    }
  }
}```
