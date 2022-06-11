Single-page site powered by jekyll
======================

## Overview
- Each vertical section is a markdown file in **_posts/** directory.
  * They're sorted by 'date' (date doesn't get used anywhere else, it only serves to sort).
- Each vertical section has it's own **color**, **header icon** (or image), **title**, and easy-to-write markdown body.
- Only **two things** to edit:
  1. Edit `_config.yml` to set the site title, description, etc
  2. Add (or edit) files under _posts/ to control each vertical section.

## Usage
- Edit `_config.yml` to change the site title, keywords, and description.
- Create a new file in `_posts/` called `yyyy-mm-dd-subject.md` where:
  - yyyy-mm-dd needs to be set according to the current list of posts (and where you want this one to be included).
  - Example: as of this update creating '2000-01-08-newsection.md' would create a new section at the end/bottom of the page. Easy!
- Some example posts and code:
~~~
  ---
  title: "home"
  bg: white     #defined in _config.yml, can use html color like '#010101'
  color: black  #text color
  style: center
  ---

  # Example headline!
  and so on..
~~~
~~~
  ---
  title: "Art"
  bg: turquoise  #defined in _config.yml, can use html color like '#0fbfcf'
  color: white   #text color
  fa-icon: paint-brush
  ---

  #### A new section- oh the humanity!
~~~

**Important:** The fa-icon header has two important notes:
1. The property (eg. `fa-icon: paint-brush`) uses a font-awesome icon (in the example above, it is [paint-brush](http://fortawesome.github.io/Font-Awesome/icon/paint-brush/)). You can use any icon from this [font-awesome icon directory](https://fortawesome.com/sets/font-awesome-4).
2. fa-icon is not used/needed for the first post/section of the site. That first "divider" icon you see is defined in the first "home" post by using a 'hidden' <span> (it's not actually hidden but you won't see the span until you begin editing the post). That <span> section currently looks like:
 ~~~
 <span class="fa-stack subtlecircle" style="font-size:100px; background:rgba(144,238,144,0.1)">
  <i class="fa fa-circle fa-stack-2x text-white"></i>
  <i class="fa fa-home fa-stack-1x text-green"></i>
</span>
 ~~~


## Changing your colors

- In each post file you can define `bg: mycolor` and `color: myothercolor` to change the background and text colors for that section.
- **mycolor** can be a quoted html color like `'#0fbfcf'` or a key to a special color defined in **_config.yml** under 'colors'.
  - **Note:** Changes to _config.yml require a manual restart to your local server with `^C` and `jekyll serve -w`.

## Extra stuff
- Add in a centered picture using something like this is a post.md
```
<center>
<img src="img/icons8-home-512.png" alt="Home Icon" title="Icons8 Home Icon" />
</center>
```
