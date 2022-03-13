# Touchpad Scrolling in Firefox on Fedora 35

Touchpad scrolling in Firefox on Fedora 35 is too fast.  
The bugs are debated [here](https://bugzilla.mozilla.org/show_bug.cgi?id=1610477), [here](https://bugzilla.mozilla.org/show_bug.cgi?id=1752862) and [here](https://bugzilla.mozilla.org/show_bug.cgi?id=1753033)

For me until this is sorted out following [solution](https://bugzilla.mozilla.org/show_bug.cgi?id=1610477#c11) worked like a charm:

- navigate to `about:config`
- set:
    - `mousewheel.default.delta_multiplier_x` = `30`
    - `mousewheel.default.delta_multiplier_y` = `30`
    - `mousewheel.default.delta_multiplier_z` = `30`

I didn't change `mousewheel.min_line_scroll_amount` as suggested in the comment, since I don't use my laptop with a mouse very often.