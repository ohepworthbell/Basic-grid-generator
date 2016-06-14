# Basic-grid-generator
A very basic, light-weight SCSS-powered grid generator

There are some great SCSS grid generators out there, with great features and expandability. But sometimes you just want something incredibly simple and light-weight for creating basic grids. This is just that - basically a plug-and play grid generator. Supports IE9+ (due to use of CSS3 calc()) and the latest release all other major browsers.

The grid generator essentially prints out straight, homogenous grids (i.e. single columns, with no cell-merging, etc.) and works by a .col- prefix and a number of how many columns, i.e.


### Example usage ###
The grid generator is plug and play, so if you include the .scss files, then all you need to do is write

In your scss root file
```
@import 'grid.scss';
```

In your HTML
```
<div class="row">
  <div class="col-3">
    This is a column
  </div>

  <div class="col-3">
    This is a column
  </div>

  <div class="col-3">
    This is a column
  </div>

  <div class="clear"></div>
```

This will print out a grid with 3 columns. That's it!

Remember to include a "clear" tag for floated elements. This grid generator does not use flexbox due to limited backward support (looking at you, IE).


### Changing settings ###
You can set how many columns are generated in the `_settings.scss` file by changing the `$grid_count` variable, and the guttering between columns via the `$grid_gutter` variable. By default, the generator will generate columns between 2 and 6 with a guttering of 20px, but can in fact be used to generate essentially an unlimited number of columns, with any sized guttering (assuming that the guttering isn't wider than the column widths, obviously).


### Who to thank ###
No one. This grid generator likely does nothing for you! The whole thing is scrappy as sin, and very basic, but it might be interesting for anyone wanting to develop their own grid generator and wants to see how loops can be used in the process.


### Going forwards ###
There are many grid generators out there that have a lot of functionality, and fully-fledged features that allow you to have proper masonry and "isotope" layouts - sometimes there is no point re-inventing the wheel. If you're just making a small website and want a quick, no-frills generator for making a few triple-columned grids, this might do you well. But I have no current plans to develop this any further :(
