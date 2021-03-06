# Vanilla JS Modal

### Simple modal built in ~30 lines of vanilla JS

[Click here for live code pen demo](https://codepen.io/RileyB/full/XQyaXy)

![Modal](readme.gif)

# Usage:

All you need is the code from the `style.css`, `main.js` and the following HTML structure

```html
<div class="modal-content-wrapper">
  <div class="image-modal-content">
    <img
      src="img/placeholder-1.jpg"
      data-title="My Cool Title"
      data-description="This is a super cool description"
      data-url="https://riley.gg/"
      data-repo="https://github.com/Riley-Brown"
      alt="Vanilla JS Modal"
    />
  </div>
</div>
```

This div `.modal-content-wrapper` will hold the content you want inside the modal on click. Each individual item must be inside the `.image-modal-content` class.

You will also need this div which is the actual modal popup and content inside of it

```html
<div class="image-modal-popup">
  <div class="wrapper">
    <span>&times;</span>
    <img src="" alt="Image Modal" />
    <div class="description">
      <h1>This is placeholder content</h1>
      <p>This content will be overwritten when the modal opens</p>
      <a href="#" target="_blank" rel="noopener noreferrer">View Cool Link</a>
      <a
        href="#"
        class="secondary-link"
        target="_blank"
        rel="noopener noreferrer"
        >View Another Link</a
      >
    </div>
  </div>
</div>
```

HTML5 data attributes are being used for the dynamic image info such as `data-title` and `data-description`. If you don't want these extra properties simply remove the following from the `main.js` file:

```js
modalElement('h1').innerHTML = data.title;
modalElement('p').innerHTML = data.description;
modalElement('a').href = data.url;
modalElement('.secondary-link').href = data.repo;
```

The current layout is styled to be 3 row columns, this can be easily changed by adjusting the flex property on the `.image-modal-content` class

```css
.modal-content-wrapper .image-modal-content {
  flex: 0 0 30%;
}
```
