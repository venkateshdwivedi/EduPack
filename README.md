# EduPack rough installation HowTo

You need a functioning installation of TVB either from git (https://github.com/the-virtual-brain/tvb-pack) or the official release (http://thevirtualbrain.org/tvb/zwei/app). We recommend to use the release version so far. EduPack has been tested with TVB 1.3.

## To install EduPack, copy the following files from EduPack.git:

* EduPack.git/tvb-framework/tvb/interfaces/web/ (EduPack base path)
 * static/js/edupack
 * static/style/base.css
 * static/style/edupack.css
 * static/style/img/edupack
 * static/style/img/nav/icon_nav_edu*
 * templates/genshi/edupack_template.html
 * templates/genshi/base_template.html
 * templates/genshi/footer.html

To your TVB installation base path:

* Linux: TVB_Distribution/tvb_data/tvb/interfaces/web
* OS X: /Applications/TVB_Distribution/tvb.app/Contents/Resources/lib/python2.7/tvb/interfaces/web
* Windows: accordingly

For instance,

```
EDU_BASE=./EduPack.git/tvb-framework/tvb/interfaces/web
TVB_BASE=./TVB_Distribution/tvb_data/tvb/interfaces/web
rsync -av $EDU_BASE/static/js/edupack $TVB_BASE/static/js/
rsync -av $EDU_BASE/static/style/{base.css,edupack.css} $TVB_BASE/static/style/
rsync -av $EDU_BASE/static/style/img/edupack $TVB_BASE/static/style/img/
rsync -av $EDU_BASE/static/style/img/nav/*edu* $TVB_BASE/static/style/img/nav/
rsync -av $EDU_BASE/templates/genshi/{base_template.html,edupack_template.html,footer.html} $TVB_BASE/templates/genshi/
```

## Then start TVB

EduPack will be visible under e.g. "Simulator" tab down to the right. It will interactively guide you through the use of TVB.

## Help us make it better

Please tell us how we can improve EduPack. If you have specific comments or found a bug, please use GitHub Issues or fork this repo and send a pull request with your improvements.
