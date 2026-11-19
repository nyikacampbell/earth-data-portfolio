# Nyika Campbell's Earth Data Portfolio
## *earth-data-portfolio*
A personal portfolio website showcasing coding and mapping projects Nyika develops as part of the Earth Data Analytics certificate program at the University of Colorado Boulder.


## General Repo Naming Convention
* `coding-assignments` folder contains all the coded notebooks that generate posts 
  * assignments have a two-number `01_` prefix followed by the assignment `shortname`
  * assignment folders have 3 typical sub folders
    * `data` git-ignored holds downloaded data and generated data and may have sub-folders
    * `figures` holds generated figures
      * excluding those that are used in posts, or index which are written directly to the `img` folder.
    * `notebooks` holds the notebooks for the assignment
      * portfolio post html are written directly from notebook to the `portfolio-posts` folder
* portfolio posts start with their one word `shortname_` 
* Post tile and description is concise and uses `kebab-case`
* images used in the post start with `post_shortname_` index images start with `index_`
* images need to have the same file extension. use `.jpg` 

## Folder and File Layout

```
earth-data-portfolio/
├── coding-assignments/
│   └── 01_shortname/
│       ├── data/                        * Git-ignored
│       ├── figures/
│       └── notebooks/
├── portfolio-posts/
│   └── shortname_post-title.html        * Written here by notebooks
├── img/
│   └── post_shortname_image-name.png    * Figures images written here by notebooks
│   └── index_image-name.png
```