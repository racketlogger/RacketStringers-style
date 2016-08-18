#/r/RacketStringers stylesheet
This is the stylesheet used on http://www.reddit.com/r/RacketStringers. It is written in [SASS](http://sass-lang.com) (Syntactically Awesome Stylesheets) and has been compiled to CSS for use on Reddit. It was originally 

##Using the stylesheet
If you'd like to test out changes to the stylesheet yourself (for example before submitting a pull request or if you're interested in using a modified version on your own subreddit, here's an overview of how to do it.

###Download the code
You can either download a [zip archive](https://github.com/awkisopen/reddit-writing-stylesheet/archive/master.zip) or clone this repository using `git`:

    git clone git://git@github.com/awkisopen/reddit-writing-stylesheet

###Install SASS
The SASS installation directions can be found at http://sass-lang.com/tutorial.html.

###Upload images
If you're looking to replicate the entire stylesheet including its header image and custom icons, you can find those in `header/` and `icons/` respectively.

Upload the header image by navigating to `http://www.reddit.com/r/name_of_subreddit/about/edit` and press the upload button under "look and feel". If it's a different height than the header image on /r/writing, you'll want to change `$header-height` in `style.scss`.

The rest of the icons, along with the header background, should be uploaded on the CSS stylesheet page, `http://www.reddit.com/r/name_of_subreddit/about/stylesheet`. If you have your own icons, make sure they have a dimension of 50x50 pixels and adjust `elements/flair.scss` accordingly. Reddit will fail to validate the CSS if there is a reference to an image that hasn't been uploaded or uploaded under the wrong name.

###Compile the stylesheet
Once you've got SASS, open up a command line, navigate to the place you've dumped this repository to and run:

    sass style.scss:style.css

This will produce a file called `style.css` in the same directory. As the extension implies, this is pure CSS that can be copied directly into the subreddit.

If you'd like SASS to recompile the CSS automatically whenever you make a change, you can instead run:

    sass --watch style.scss:style.css

In future, there may be a script that takes some parameters and immediately uploads the correctly parsed CSS to your subreddit. But, much like the future, we're not there yet!

##Issues
If you spot a bug in the stylesheet, have a great idea for something, or just want to know if something is possible, you can contact us in one of two ways.

The first and preferred way of getting in touch is to [create a new issue](https://github.com/awkisopen/reddit-writing-stylesheet/issues). While this requires a github account, it is the easiest way for us to keep track of issues and feature requests as they come up, and the easiest way for us to keep you informed about them.

The second way is through [modmail](http://www.reddit.com/message/compose?to=%2Fr%2Fwriting) on /r/writing. Anything reported via modmail will get its own issue opened on github and will be updated there so as not to spam up our inbox or yours.

##Credits
This theme was derived from that of the [Writing theme](http://www.reddit.com/r/writing). If you want a clean, easy-to-deploy Reddit stylesheet, check out [the Boxed project](https://github.com/creesch/Boxed-css-theme-for-reddit) on github.

Flair icons by http://www.iconarchive.com/show/trainee-icons-by-emey87.html

