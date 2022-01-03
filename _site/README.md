# Marat

![Marat](https://raw.githubusercontent.com/JohnCoene/marat/master/assets/img/screenshot.png)

---

# Fork info

### Usage

Added the usual npm scripts:

```bash
npm run dev				# bundle exec jekyll serve --watch
npm run build			# bundle exec jekyll build
```

### Install

This is what I had to run to make this work.

##### Installing Jekyll

```bash
export SDKROOT=$(xcrun --show-sdk-path)
gem install --user-install bundler jekyll
```

I got the following error but choose to ignore it:

```
Parsing documentation for jekyll-4.2.1
Before reporting this, could you check that the file you're documenting
has proper syntax:

  /System/Library/Frameworks/Ruby.framework/Versions/2.6/usr/bin/ruby -c lib/jekyll/commands/doctor.rb

RDoc is not a full Ruby parser and will fail when fed invalid ruby programs.

The internal error was:

	(NoMethodError) undefined method `[]' for nil:NilClass

ERROR:  While executing gem ... (NoMethodError)
    undefined method `[]' for nil:NilClass
```

See here for more info: [Jekyll & macOS](https://jekyllrb.com/docs/troubleshooting/#jekyll--macos)

##### Installing dependencies

This also failed:

```bash
bundle install
```

Error:

```
An error occurred while installing ffi (1.9.18), and Bundler cannot continue.
```

Fixed it by running:

```bash
bundle update
```

### Build/watch

This finally worked:

```bash
bundle exec jekyll serve --watch
```

---

Revive the values of the Enlightenment with `marat`.

See [Marat in action](http://marat.john-coene.com).

Marat is heavily inspired by [L'Ami du peuple](https://en.wikipedia.org/wiki/L%27Ami_du_peuple), a newspaper written by [Jean-Paul Marat](https://en.wikipedia.org/wiki/Jean-Paul_Marat) during the French Revolution, in which he was a j vocal advocate for the rights of man and liberty.

1. Adapt the `_config.yml` file
2. Replace/Delete the posts
3. Change `about.md`
4. Change or add your links in the `nav.yml` file located in the `_data` folder
5. Replace the `favicon.ico`
6. Customise the `404.md` page in the root directory
7. Run `bundle exec jekyll serve --watch`
8. Enlighten the masses!

> Unlike Marat's pamphlets the theme is fully responsive.

Plugins:

Marat includes the following plugins.

-   [jekyll-roman](https://github.com/paulrobertlloyd/jekyll-roman)
-   [jekyll-seo-tag](https://github.com/jekyll/jekyll-seo-tag)
