With this module, you can create "merge tags" in [ApostropheCMS](https://apostrophecms.org)...

<p align="center"><img src="https://raw.githubusercontent.com/apostrophecms/apostrophe-rich-text-merge-tags/master/screenshots/screenshot-1.png" /></p>

<p align="center"><img src="https://raw.githubusercontent.com/apostrophecms/apostrophe-rich-text-merge-tags/master/screenshots/screenshot-2.png" /></p>

Then you and your editors can insert them into any rich text widget...

<p align="center"><img src="https://raw.githubusercontent.com/apostrophecms/apostrophe-rich-text-merge-tags/master/screenshots/screenshot-3.png" /></p>

<p align="center"><img src="https://raw.githubusercontent.com/apostrophecms/apostrophe-rich-text-merge-tags/master/screenshots/screenshot-4.png" /></p>

<p align="center"><img src="https://raw.githubusercontent.com/apostrophecms/apostrophe-rich-text-merge-tags/master/screenshots/screenshot-5.png" /></p>

And **if you change the value of the tag later, that will automatically be reflected on the page.**

Of course, ordinary site visitors see them as ordinary text with no special styling.

<p align="center"><img src="https://raw.githubusercontent.com/apostrophecms/apostrophe-rich-text-merge-tags/master/screenshots/screenshot-6.png" /></p>

Line breaks are allowed in the values of merge tags. No other formatting is permitted.

## Installation

```
npm install apostrophe-rich-text-merge-tags
```

```
// in app.js
modules: {
  'apostrophe-rich-text-merge-tags': {}
}
```

```
{# In the page template where you want to allow this feature
 in a rich text widget. The important thing here is adding
 "Mergetag" to your toolbar. Note the "M" is capitalized. #}

{{
  apos.area(data.page, 'body', {
    widgets: {
      'apostrophe-rich-text': {
        toolbar: [ 'Styles', 'Bold', 'Italic', 'Mergetag' ]
      },
      'apostrophe-images': {}
    }
  })
}}
```

Requires Apostrophe `2.66.0` or better.
