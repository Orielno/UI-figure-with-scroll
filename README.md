# UI-figure-with-scroll
A MATLAB function that creates a User Interface figure with given height and width, and also the maximum height of the figure in terms of percentage of the computer screen's height. If the required height of the figure is bigger than the given percentage of the screen, the figure will have a scroll. Otherwise, it won't have a scroll, as it is not needed. This is useful for cases when the figure is not too big in some computers (no need for scroll), but is too big in other computers (hence a scroll is needed). I originally programmed this function as a part of the "RP-Toolkit" package, but it can be used anywhere else as well.

**Usage:**
[base_figure, base_panel] = ui_scroll_screen(figure_width, figure_height, scroll_width, max_height_percent, top_space_height, bottom_space_height, title)

**output**
* base_figure - the figure itself, which contains the "base_panel", the "bottom_space_height" area and the "top_space_height" area.
* base_panel - contained inside "base_figure", and it is being scrolled (when there is a scroll).

**input**
* figure_width - the figure's width. if there is a scroll, the figure's width is: figure_width + scroll_width.
* figure_height - the figure's height, assuming it is not more than: max_height_percent * computer screen's height.
* scroll_width - the width of the scroll object.
* max_height_percent - if "figure_height" is more than this times the screen's height, than the figure's height will be set to exactly this variable times the screen's height, and a scroll will be in place. otherwise, there will be no scroll.
* top_space_height - height of area in top of figure that is fixed and is not scrolled. if such space is not needed, enter 0.
* bottom_space_height - height of area in bottom of figure that is fixed and is not scrolled (in RP-toolkit, this area contained the "OK" and "Cancel" buttons in the bottom). if such space is not needed, enter 0.
* title - title of the figure to be displayed.
