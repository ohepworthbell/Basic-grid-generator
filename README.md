# Basic-grid-generator
A basic SCSS-powered grid generator.

There are some great SCSS grid generators out there, with great features and expandability. But sometimes you just want something really simple and light-weight for creating basic grids. This is just that - a plug-and-play grid generator for simple columned layouts, without any bells and whistles. Supports IE9+ (due to use of CSS3 `calc()`) and the latest release all other major browsers.

The grid generator essentially prints out straight, homogenous grids (i.e. single columns, with no cell-merging, etc.) and works by a `.col-` prefix and a column count, e.g.

```scss
.element-wrapper {
  @include create_grid(<gutter-size-pixels>, <column-count>);
}

```


### Example usage ###
The grid generator is plug and play, so if you include the .scss files, then all you need to do is write

In your scss root file
```scss
@import '_settings.scss';
// No need to import grid.scss, as this is already imported in _settings

.your-element-name {
  @extend %clear;
  @include create_grid($grid_gutter, 3);
  }

.another-element-name {
  @extend %clear;
  @include create_grid($grid_gutter, 2);
  }
```

In your HTML
```html
<div class="your-element-name">
  <div class="col-3">
    This is a column
  </div>

  <div class="col-3">
    This is a column
  </div>

  <div class="col-3">
    This is a column
  </div>
</div>

<div class="another-element-name">
  <div class="col-2">
    This is a column
  </div>

  <div class="col-2">
    This is a column
  </div>
</div>
```

This will print out a grid with columns. That's it!


### Should I use this ###
Probably not. This grid generator was made for 2 reasons. The first is that sometimes it's just quicker to use a very basic method like this, which doesn't clog up the system too much, and in nice, simple and manageable for small, basic websites.

The other is practice, from my early days of learning and developing my SCSS knowledge. In that regard, it has served me well.


### Going forwards ###
There are many grid generators out there that have a lot of functionality, and fully-fledged features that allow you to have proper masonry and "isotope" layouts - sometimes there is no point re-inventing the wheel. If you're just making a small website and want a quick, no-frills, no-setup-required generator for making a few multi-columned grids, this might do you well. But I have no current plans to develop this much further :(
