# CLHENRICK
Personal portfolio and blog of Chris Henrick using the [Feeling Resposive](http://phlow.github.io/feeling-responsive/) Jekyll theme. Forked from [Phlow](https://github.com/Phlow/feeling-responsive)

## Migrating Portfolio
To migrate work from an existing portfolio I created `JSON` data containing information for each project. This data lives in `_data/work.json` and is used to generate each page for a project as well as created the portfolio overview page.

Updating the portfolio works like this:  

1. Edit `_data/work.json` as needed.
2. `cd scripts/ && npm install`
3. from the `scripts/` dir do `node make-portfolio-posts.js`

To run Jekyll in a dev environment do:  
`jekyll serve --config _config.yml,_config_dev.yml`

## Updating
Add a new object to `_data/work.json` containing the following:

```
"title" : "Prospect Park non euclidean map", // required: title of the project
"tags" : ["carto"], // required: any relevant tags
"description" : "A \"non-euclidean map\" of Prospect Park, Brooklyn", // short description shown in `/work/`
"description_long" : "A non-euclidean “map” of Prospect Park, Brooklyn. Created using a GoPro camera mounted to my head, iMovie for video editing and Open-Frameworks for combining the video shots into one screen space. Inspired by the theory of artist and cartographer Dennis Wood and work by Annette Kim, Associate Professor of Urban Studies and Planning at <a href=\"http://slab.scripts.mit.edu/wp/maps/narrative-maps/\">MIT's SLAB</a>", // long description shown in the corresponding project page
"thumb" : "ppnc-thumb.jpg", // required: thumb nail image
"tech" : ["Go-Pro","OpenFrameworks"], // whatever tech was used
"video" : {
"url" : "https://vimeo.com/81728484", // link to a video if the project has one
"embed" : "https://player.vimeo.com/video/81728484" // link to the embed url for the video
},
"imgs" : ["ppnc.jpg"], // required: any images associated with the project
"size" : "width2 ", // size to give to the project (depreciated / unnecessary)
"date" : "2013-12-16" // date the project was created
```

Then `cd` to the `scripts` dir and do `node make-portfolio-pages.js`

## TO DO List:
- [x] Make thumbnails & resize images

- [x] Make portfolio mobile friendly

- [ ] add presentations as a git sub-module

- [ ] add CV / Resume

- [ ] add Talks

- [x] Node JS script to generate posts in `_posts/portfolio/` from `assets/data/work.json`

- [x] ~~liquid logic to only render blog posts in `_posts/blog/`~~

- [x] liquid logic to create masonry layout from `_posts/portfolio/`

- [ ] move blog posts from chenrickmfadt.wordpress:  
    - see: http://import.jekyllrb.com/docs/wordpress/
    - see: https://wordpress.org/plugins/jekyll-exporter/
    - do: `gem install unidecode sequel mysql2 htmlentities`
    - do: `gem install jekyll-import`
    - see: https://github.com/jekyll/jekyll-import/blob/v0.7.1/lib/jekyll-import/importers/wordpress.rb

- [x] move site to clhenrick.io(?)

- [ ] ~~forward chrishenrick.com to clhenrick.io(?)~~

- [x] add portfolio images for print work
    - [x] resize existing images to be smaller file size
    - [x] create thumbnails for them? Probably depends on masonry.js
    
- [x] add portfolio projects for web work (AIRS, Bushwick, Toxicity Map, etc)

- [ ] create a logo!

- [ ] generate favicons & touch icons from logo using [real favicon generator](http://realfavicongenerator.net/)

- [ ] index with Google’s SEO & custom search using sitemap.xml

## Deploying Jekyll With Git On A Remote VPS
- https://www.digitalocean.com/community/tutorials/how-to-deploy-jekyll-blogs-with-git
- https://www.digitalocean.com/community/tutorials/how-to-get-started-with-jekyll-on-an-ubuntu-vps

## Helpful Architecture Info:
### jekyll
- http://jekyllrb.com/docs/variables/
- http://pixelcog.com/blog/2013/jekyll-from-scratch-core-architecture/

### Feeling Responsive Jekyll Theme
- https://phlow.github.io/feeling-responsive/
- https://github.com/Phlow/feeling-responsive

### Foundation
- http://foundation.zurb.com/docs/components/grid.html

### Liquid
- https://github.com/Shopify/liquid/wiki/Liquid-for-Designers

### Helpful UI Stuff
#### Favicons & Touch Icons
- https://mathiasbynens.be/notes/touch-icons
- https://css-tricks.com/favicon-quiz/
- http://realfavicongenerator.net/

#### Flexible / Staggered Multiple Column Layouts:  
- http://isotope.metafizzy.co/
- http://masonry.desandro.com/


