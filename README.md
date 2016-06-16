# Sass-Google-Web-Fonts
SCSS Mixin for autogenerating Google Web Fonts

Firstly add _google_webfont.scss to your assets/stylesheets folder or where-ever you store your SCSS files.

To use the google webfonts mixin all you need to do is call the mixin and give it a web font name. So for example if you want to load Open Sans as your body copy you would do the following.

#####styles.scss
    body {
      @include webfont(Open Sans);
    }

This would output as:

#####styles.css
    body {
      @import url(https://fonts.googleapis.com/css?family=Open+Sans);
    }

If you want to add more fonts just use a comma in the include. No need for adding in the + between names, the mixin will sort that in the url for you.

For example:

#####styles.scss
    body {
      @include webfont(Open Sans, Pacifico);
    }

Would output as:

#####styles.css
    body {
      @import url(https://fonts.googleapis.com/css?family=Open+Sans|Pacifico);
    }
