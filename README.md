# ultrabit-web.github.io

ultrabit.com uses [Jekyll](https://jekyllrb.com/), a templating tool that allows plain text updates to static sites. While most of the site will still be updated by HTML, the jobs section leverages Jekyll for ease of updating. To view the site locally, you'll need to install and run Jekyll, or you can update the site blindly for small changes.

## Main Layout
The main index file lives in `_layouts/default.html`. You'll find everything on the page, like the head and body, except for the Jobs section. CSS/JS files are normally where they are found. 

## Updating Games 
* Add games through `_layouts/default.html` by copying/pasting the `<li>` containers for each game. 
* There are 2 layouts for each game - use the class `games--list--cover` on the `<li>` for a larger layout that takes up 1 full column, use class `games--list--item` for 2 columns. Be aware of total games so that you don't end up with an orphaned game at the bottom of the games list.
![ultrabit game image layouts](https://cdn3.kongcdn.com/assets/files/0002/7506/ultrabit-layout.jpg)
* Both images should be `1024px x 568px`.
* Save images to `/imgs` and update the image path.
* Change the link where you want to send the user. In the past, they've been directed to the Kongregate custom page for the game, but an Adjust URL for the game would work well, as it can direct either to the App Store or Google Play, depending on the device.

## Updating Jobs 
Jobs is updated through a Yaml file, in` _data/jobs.yaml`. The format for each job posting is commented in the file.

* Don't remove the comments whenever you update the file!
* When there are no job postings listed, the section will automatically display "No listings at this time!"
* To add a job posting, follow the format as commented in the yaml file. There are 2 fields of content: `position`, for the job title, and the `description`, which takes Markdown for formatting. 
* Remove the `#` at the start of every line before saving the file.
* Refer to past updates to see examples 
