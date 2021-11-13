# SCSS Library

A collection of SCSS' mixins and functions I use in my projects


### Idea
The main idea behind this collection is the different syntax used to pass argument to mixin. Let me show an example:

Source SCSS code
```scss
.some-class {
  @include text(ff "Arial" sans-serif, fs 2rem, fw b, lh 1.2, tt u);

  @include after(c 'hello') {
      @include position(p a, t 0, l 0);
      @include box(w 100%);
  };
}
```

Compiled CSS code
```css
.some-class {
  font-family: "Arial", sans-serif;
  font-size: 2rem;
  font-weight: bold;
  line-height: 1.2;
  text-transform: uppercase;
  position: relative;
}

.some-class::after {
  content: "hello";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
```



### Structure:
```
scss
  |-- scss2                       // collection of scss-like functions
  |     |-- _list2.scss           // collection of list-related functions
  |     |-- _map2.scss            // collection of map-related  functions
  |
  |-- abstracts                   // collection of mixins and functions
        |-- mixins                // collection of mixins
        |     |-- _index.scss     // index file
        |     |-- _box-model.scss // box model-related mixins
        |     |-- _text.scss // text-related mixins
        |
        |-- space-mixin.scss      // main mixin-builder
.gitignore
LICENSE
README.md
```
