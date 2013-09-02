
# NodeConf.eu Themed Slides

<p style="margin: 100px auto 0 auto; text-align: center; font-size: 10px;">
*(use -&gt; and &lt;- to navigate)*
</p>

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

## Browser stuff

Designed for Chrome, works well enough across other browsers for sharing afterwards.

Zoom in till it fits (Ctrl +, or whatever your OS variant is)

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

## Heading 2

### Heading 3
### &nbsp;&nbsp;&nbsp;&nbsp;&hellip; more 3rd-level heading
### &nbsp;&nbsp;&nbsp;&nbsp;&hellip; and a little more
### &nbsp;&nbsp;&nbsp;&nbsp;&hellip; just one more!

And a bit of paragraph here

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

## Authored in Markdown

Single *index.md* file (like [this one](https://raw.github.com/rvagg/campjs-2013-learn-you-node/master/src/index.md)), with a *build.js* (like [this one](https://raw.github.com/rvagg/campjs-2013-learn-you-node/master/src/build.js)) script that converts to the slides, including formatting and even syntax highlighting.

 * *build.js* also has a `--watch`

```js
var foo = require('bar')

if (foo['woohoo'] === false)
  throw new Error('Whoa!')
```

And GitHub-style `inline = code`.

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

## Break out of Markdown

Inline HTML supported so you can control styling:

<table cellpadding=0 cellspacing=0 style="border-collapse: collapse; margin: 20px auto;">
  <tr>
    <td style="border-bottom: dashed 2px rgb(134,136,118); padding: 2em; text-align: center;">Eh?</td>
    <td style="border: solid 2px rgb(134,136,118); background-color: rgb(245,245,244); padding: 2em; text-align: center;" colspan=4>Ooooo, a white box!</td>
    <td style="border-bottom: dashed 2px rgb(134,136,118); padding: 0.5em;">&nbsp;</td>
  </tr>
  <tr>
    <td style="padding: 2em; text-align: center;" rowspan=2>What is this?</td>
    <td style="border: solid 2px rgb(134,136,118); padding: 2em; text-align: center;" colspan=4>I don't know, but it's awesome!</td>
  </tr>
</table>
