% Pandoc + Reveal.js
% Marius Loewe

## Pandoc + Reveal.js

= use whatever markup language you want to create reveal.js (or S5, DZSlides, Slidy, Slideous, or LaTeX beamer) slides

# Setup

## Pandoc

`sudo apt-get install pandoc`

Or try `cabal`

## Reveal.js

`git clone https://github.com/hakimel/reveal.js.git`

## File Structure

<pre>
├── reveal.js
│   ├── ...
├── slides.md
├── slides.html
</pre>

# Markup

## Headlines

- no content with top-level headlines
    - a bit complicated
	- just put `##headlines` after `#headlines`

## New Slide

- still a bit complicated
- `#headline` -> new horizontal slide
- `##headline` -> new vertial slide
- horizontal rule -> new slide

## Incremental Lists

> - show
> - one
> - at
> - a
> - time
> - using `>` block quotes
> - or use `-i`

## Speaker Notes

    <div class="notes">
		Some Notes
	</div>

Reveal.js needs a server component for this

# Commands

## Simple

`pandoc -t revealjs -s slides.md -o slides.html`

## Variables

`pandoc -t revealjs -s slides.md -o slides.html`
`-V theme=moon -V transition=none`

## Locations

`pandoc -t revealjs -s slides.md -o slides.html`
`-V theme=moon -V transition=none`
`-V revealjs-url=../reveal.js`
`--template=../template.html`

# The Rest

## My File Structure

<pre>
├── reveal.js
│   ├── ...
├── &lt;some presentation&gt;
│   ├── slides.html
│   ├── slides.md
├── template.html
</pre>

## References
- https://github.com/nexxTM/slides/pandoc_reveal/slides.md
- http://johnmacfarlane.net/pandoc/demo/example9/producing-slide-shows-with-pandoc.html
- http://johnmacfarlane.net/pandoc/README.html
