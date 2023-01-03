# Data-visualization-using-Seaborn
Seaborn is a Python data visualization library based on matplotlib. It provides a high-level interface for drawing attractive and informative statistical graphics. Seaborn is widely used in the data science community and is particularly useful for exploring and visualizing data sets with multiple variables. It makes it easy to create complex, multi-layered graphics that can help you understand patterns and relationships in your data.
<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />

<title>seaborn</title>

<script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>



<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.7 (http://getbootstrap.com)
 * Copyright 2011-2016 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}
audio:not([controls]) {
  display: none;
  height: 0;
}
[hidden],
template {
  display: none;
}
a {
  background-color: transparent;
}
a:active,
a:hover {
  outline: 0;
}
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sup {
  top: -0.5em;
}
sub {
  bottom: -0.25em;
}
img {
  border: 0;
}
svg:not(:root) {
  overflow: hidden;
}
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}
button {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}
button[disabled],
html input[disabled] {
  cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
}
input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
  .navbar {
    display: none;
  }
  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }
  .label {
    border: 1px solid #000;
  }
  .table {
    border-collapse: collapse !important;
  }
  .table td,
  .table th {
    background-color: #fff !important;
  }
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
  content: "\20ac";
}
.glyphicon-minus:before {
  content: "\2212";
}
.glyphicon-cloud:before {
  content: "\2601";
}
.glyphicon-envelope:before {
  content: "\2709";
}
.glyphicon-pencil:before {
  content: "\270f";
}
.glyphicon-glass:before {
  content: "\e001";
}
.glyphicon-music:before {
  content: "\e002";
}
.glyphicon-search:before {
  content: "\e003";
}
.glyphicon-heart:before {
  content: "\e005";
}
.glyphicon-star:before {
  content: "\e006";
}
.glyphicon-star-empty:before {
  content: "\e007";
}
.glyphicon-user:before {
  content: "\e008";
}
.glyphicon-film:before {
  content: "\e009";
}
.glyphicon-th-large:before {
  content: "\e010";
}
.glyphicon-th:before {
  content: "\e011";
}
.glyphicon-th-list:before {
  content: "\e012";
}
.glyphicon-ok:before {
  content: "\e013";
}
.glyphicon-remove:before {
  content: "\e014";
}
.glyphicon-zoom-in:before {
  content: "\e015";
}
.glyphicon-zoom-out:before {
  content: "\e016";
}
.glyphicon-off:before {
  content: "\e017";
}
.glyphicon-signal:before {
  content: "\e018";
}
.glyphicon-cog:before {
  content: "\e019";
}
.glyphicon-trash:before {
  content: "\e020";
}
.glyphicon-home:before {
  content: "\e021";
}
.glyphicon-file:before {
  content: "\e022";
}
.glyphicon-time:before {
  content: "\e023";
}
.glyphicon-road:before {
  content: "\e024";
}
.glyphicon-download-alt:before {
  content: "\e025";
}
.glyphicon-download:before {
  content: "\e026";
}
.glyphicon-upload:before {
  content: "\e027";
}
.glyphicon-inbox:before {
  content: "\e028";
}
.glyphicon-play-circle:before {
  content: "\e029";
}
.glyphicon-repeat:before {
  content: "\e030";
}
.glyphicon-refresh:before {
  content: "\e031";
}
.glyphicon-list-alt:before {
  content: "\e032";
}
.glyphicon-lock:before {
  content: "\e033";
}
.glyphicon-flag:before {
  content: "\e034";
}
.glyphicon-headphones:before {
  content: "\e035";
}
.glyphicon-volume-off:before {
  content: "\e036";
}
.glyphicon-volume-down:before {
  content: "\e037";
}
.glyphicon-volume-up:before {
  content: "\e038";
}
.glyphicon-qrcode:before {
  content: "\e039";
}
.glyphicon-barcode:before {
  content: "\e040";
}
.glyphicon-tag:before {
  content: "\e041";
}
.glyphicon-tags:before {
  content: "\e042";
}
.glyphicon-book:before {
  content: "\e043";
}
.glyphicon-bookmark:before {
  content: "\e044";
}
.glyphicon-print:before {
  content: "\e045";
}
.glyphicon-camera:before {
  content: "\e046";
}
.glyphicon-font:before {
  content: "\e047";
}
.glyphicon-bold:before {
  content: "\e048";
}
.glyphicon-italic:before {
  content: "\e049";
}
.glyphicon-text-height:before {
  content: "\e050";
}
.glyphicon-text-width:before {
  content: "\e051";
}
.glyphicon-align-left:before {
  content: "\e052";
}
.glyphicon-align-center:before {
  content: "\e053";
}
.glyphicon-align-right:before {
  content: "\e054";
}
.glyphicon-align-justify:before {
  content: "\e055";
}
.glyphicon-list:before {
  content: "\e056";
}
.glyphicon-indent-left:before {
  content: "\e057";
}
.glyphicon-indent-right:before {
  content: "\e058";
}
.glyphicon-facetime-video:before {
  content: "\e059";
}
.glyphicon-picture:before {
  content: "\e060";
}
.glyphicon-map-marker:before {
  content: "\e062";
}
.glyphicon-adjust:before {
  content: "\e063";
}
.glyphicon-tint:before {
  content: "\e064";
}
.glyphicon-edit:before {
  content: "\e065";
}
.glyphicon-share:before {
  content: "\e066";
}
.glyphicon-check:before {
  content: "\e067";
}
.glyphicon-move:before {
  content: "\e068";
}
.glyphicon-step-backward:before {
  content: "\e069";
}
.glyphicon-fast-backward:before {
  content: "\e070";
}
.glyphicon-backward:before {
  content: "\e071";
}
.glyphicon-play:before {
  content: "\e072";
}
.glyphicon-pause:before {
  content: "\e073";
}
.glyphicon-stop:before {
  content: "\e074";
}
.glyphicon-forward:before {
  content: "\e075";
}
.glyphicon-fast-forward:before {
  content: "\e076";
}
.glyphicon-step-forward:before {
  content: "\e077";
}
.glyphicon-eject:before {
  content: "\e078";
}
.glyphicon-chevron-left:before {
  content: "\e079";
}
.glyphicon-chevron-right:before {
  content: "\e080";
}
.glyphicon-plus-sign:before {
  content: "\e081";
}
.glyphicon-minus-sign:before {
  content: "\e082";
}
.glyphicon-remove-sign:before {
  content: "\e083";
}
.glyphicon-ok-sign:before {
  content: "\e084";
}
.glyphicon-question-sign:before {
  content: "\e085";
}
.glyphicon-info-sign:before {
  content: "\e086";
}
.glyphicon-screenshot:before {
  content: "\e087";
}
.glyphicon-remove-circle:before {
  content: "\e088";
}
.glyphicon-ok-circle:before {
  content: "\e089";
}
.glyphicon-ban-circle:before {
  content: "\e090";
}
.glyphicon-arrow-left:before {
  content: "\e091";
}
.glyphicon-arrow-right:before {
  content: "\e092";
}
.glyphicon-arrow-up:before {
  content: "\e093";
}
.glyphicon-arrow-down:before {
  content: "\e094";
}
.glyphicon-share-alt:before {
  content: "\e095";
}
.glyphicon-resize-full:before {
  content: "\e096";
}
.glyphicon-resize-small:before {
  content: "\e097";
}
.glyphicon-exclamation-sign:before {
  content: "\e101";
}
.glyphicon-gift:before {
  content: "\e102";
}
.glyphicon-leaf:before {
  content: "\e103";
}
.glyphicon-fire:before {
  content: "\e104";
}
.glyphicon-eye-open:before {
  content: "\e105";
}
.glyphicon-eye-close:before {
  content: "\e106";
}
.glyphicon-warning-sign:before {
  content: "\e107";
}
.glyphicon-plane:before {
  content: "\e108";
}
.glyphicon-calendar:before {
  content: "\e109";
}
.glyphicon-random:before {
  content: "\e110";
}
.glyphicon-comment:before {
  content: "\e111";
}
.glyphicon-magnet:before {
  content: "\e112";
}
.glyphicon-chevron-up:before {
  content: "\e113";
}
.glyphicon-chevron-down:before {
  content: "\e114";
}
.glyphicon-retweet:before {
  content: "\e115";
}
.glyphicon-shopping-cart:before {
  content: "\e116";
}
.glyphicon-folder-close:before {
  content: "\e117";
}
.glyphicon-folder-open:before {
  content: "\e118";
}
.glyphicon-resize-vertical:before {
  content: "\e119";
}
.glyphicon-resize-horizontal:before {
  content: "\e120";
}
.glyphicon-hdd:before {
  content: "\e121";
}
.glyphicon-bullhorn:before {
  content: "\e122";
}
.glyphicon-bell:before {
  content: "\e123";
}
.glyphicon-certificate:before {
  content: "\e124";
}
.glyphicon-thumbs-up:before {
  content: "\e125";
}
.glyphicon-thumbs-down:before {
  content: "\e126";
}
.glyphicon-hand-right:before {
  content: "\e127";
}
.glyphicon-hand-left:before {
  content: "\e128";
}
.glyphicon-hand-up:before {
  content: "\e129";
}
.glyphicon-hand-down:before {
  content: "\e130";
}
.glyphicon-circle-arrow-right:before {
  content: "\e131";
}
.glyphicon-circle-arrow-left:before {
  content: "\e132";
}
.glyphicon-circle-arrow-up:before {
  content: "\e133";
}
.glyphicon-circle-arrow-down:before {
  content: "\e134";
}
.glyphicon-globe:before {
  content: "\e135";
}
.glyphicon-wrench:before {
  content: "\e136";
}
.glyphicon-tasks:before {
  content: "\e137";
}
.glyphicon-filter:before {
  content: "\e138";
}
.glyphicon-briefcase:before {
  content: "\e139";
}
.glyphicon-fullscreen:before {
  content: "\e140";
}
.glyphicon-dashboard:before {
  content: "\e141";
}
.glyphicon-paperclip:before {
  content: "\e142";
}
.glyphicon-heart-empty:before {
  content: "\e143";
}
.glyphicon-link:before {
  content: "\e144";
}
.glyphicon-phone:before {
  content: "\e145";
}
.glyphicon-pushpin:before {
  content: "\e146";
}
.glyphicon-usd:before {
  content: "\e148";
}
.glyphicon-gbp:before {
  content: "\e149";
}
.glyphicon-sort:before {
  content: "\e150";
}
.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}
.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}
.glyphicon-sort-by-order:before {
  content: "\e153";
}
.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}
.glyphicon-sort-by-attributes:before {
  content: "\e155";
}
.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}
.glyphicon-unchecked:before {
  content: "\e157";
}
.glyphicon-expand:before {
  content: "\e158";
}
.glyphicon-collapse-down:before {
  content: "\e159";
}
.glyphicon-collapse-up:before {
  content: "\e160";
}
.glyphicon-log-in:before {
  content: "\e161";
}
.glyphicon-flash:before {
  content: "\e162";
}
.glyphicon-log-out:before {
  content: "\e163";
}
.glyphicon-new-window:before {
  content: "\e164";
}
.glyphicon-record:before {
  content: "\e165";
}
.glyphicon-save:before {
  content: "\e166";
}
.glyphicon-open:before {
  content: "\e167";
}
.glyphicon-saved:before {
  content: "\e168";
}
.glyphicon-import:before {
  content: "\e169";
}
.glyphicon-export:before {
  content: "\e170";
}
.glyphicon-send:before {
  content: "\e171";
}
.glyphicon-floppy-disk:before {
  content: "\e172";
}
.glyphicon-floppy-saved:before {
  content: "\e173";
}
.glyphicon-floppy-remove:before {
  content: "\e174";
}
.glyphicon-floppy-save:before {
  content: "\e175";
}
.glyphicon-floppy-open:before {
  content: "\e176";
}
.glyphicon-credit-card:before {
  content: "\e177";
}
.glyphicon-transfer:before {
  content: "\e178";
}
.glyphicon-cutlery:before {
  content: "\e179";
}
.glyphicon-header:before {
  content: "\e180";
}
.glyphicon-compressed:before {
  content: "\e181";
}
.glyphicon-earphone:before {
  content: "\e182";
}
.glyphicon-phone-alt:before {
  content: "\e183";
}
.glyphicon-tower:before {
  content: "\e184";
}
.glyphicon-stats:before {
  content: "\e185";
}
.glyphicon-sd-video:before {
  content: "\e186";
}
.glyphicon-hd-video:before {
  content: "\e187";
}
.glyphicon-subtitles:before {
  content: "\e188";
}
.glyphicon-sound-stereo:before {
  content: "\e189";
}
.glyphicon-sound-dolby:before {
  content: "\e190";
}
.glyphicon-sound-5-1:before {
  content: "\e191";
}
.glyphicon-sound-6-1:before {
  content: "\e192";
}
.glyphicon-sound-7-1:before {
  content: "\e193";
}
.glyphicon-copyright-mark:before {
  content: "\e194";
}
.glyphicon-registration-mark:before {
  content: "\e195";
}
.glyphicon-cloud-download:before {
  content: "\e197";
}
.glyphicon-cloud-upload:before {
  content: "\e198";
}
.glyphicon-tree-conifer:before {
  content: "\e199";
}
.glyphicon-tree-deciduous:before {
  content: "\e200";
}
.glyphicon-cd:before {
  content: "\e201";
}
.glyphicon-save-file:before {
  content: "\e202";
}
.glyphicon-open-file:before {
  content: "\e203";
}
.glyphicon-level-up:before {
  content: "\e204";
}
.glyphicon-copy:before {
  content: "\e205";
}
.glyphicon-paste:before {
  content: "\e206";
}
.glyphicon-alert:before {
  content: "\e209";
}
.glyphicon-equalizer:before {
  content: "\e210";
}
.glyphicon-king:before {
  content: "\e211";
}
.glyphicon-queen:before {
  content: "\e212";
}
.glyphicon-pawn:before {
  content: "\e213";
}
.glyphicon-bishop:before {
  content: "\e214";
}
.glyphicon-knight:before {
  content: "\e215";
}
.glyphicon-baby-formula:before {
  content: "\e216";
}
.glyphicon-tent:before {
  content: "\26fa";
}
.glyphicon-blackboard:before {
  content: "\e218";
}
.glyphicon-bed:before {
  content: "\e219";
}
.glyphicon-apple:before {
  content: "\f8ff";
}
.glyphicon-erase:before {
  content: "\e221";
}
.glyphicon-hourglass:before {
  content: "\231b";
}
.glyphicon-lamp:before {
  content: "\e223";
}
.glyphicon-duplicate:before {
  content: "\e224";
}
.glyphicon-piggy-bank:before {
  content: "\e225";
}
.glyphicon-scissors:before {
  content: "\e226";
}
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
  content: "\20bd";
}
.glyphicon-scale:before {
  content: "\e230";
}
.glyphicon-ice-lolly:before {
  content: "\e231";
}
.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}
.glyphicon-education:before {
  content: "\e233";
}
.glyphicon-option-horizontal:before {
  content: "\e234";
}
.glyphicon-option-vertical:before {
  content: "\e235";
}
.glyphicon-menu-hamburger:before {
  content: "\e236";
}
.glyphicon-modal-window:before {
  content: "\e237";
}
.glyphicon-oil:before {
  content: "\e238";
}
.glyphicon-grain:before {
  content: "\e239";
}
.glyphicon-sunglasses:before {
  content: "\e240";
}
.glyphicon-text-size:before {
  content: "\e241";
}
.glyphicon-text-color:before {
  content: "\e242";
}
.glyphicon-text-background:before {
  content: "\e243";
}
.glyphicon-object-align-top:before {
  content: "\e244";
}
.glyphicon-object-align-bottom:before {
  content: "\e245";
}
.glyphicon-object-align-horizontal:before {
  content: "\e246";
}
.glyphicon-object-align-left:before {
  content: "\e247";
}
.glyphicon-object-align-vertical:before {
  content: "\e248";
}
.glyphicon-object-align-right:before {
  content: "\e249";
}
.glyphicon-triangle-right:before {
  content: "\e250";
}
.glyphicon-triangle-left:before {
  content: "\e251";
}
.glyphicon-triangle-bottom:before {
  content: "\e252";
}
.glyphicon-triangle-top:before {
  content: "\e253";
}
.glyphicon-console:before {
  content: "\e254";
}
.glyphicon-superscript:before {
  content: "\e255";
}
.glyphicon-subscript:before {
  content: "\e256";
}
.glyphicon-menu-left:before {
  content: "\e257";
}
.glyphicon-menu-right:before {
  content: "\e258";
}
.glyphicon-menu-down:before {
  content: "\e259";
}
.glyphicon-menu-up:before {
  content: "\e260";
}
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
a {
  color: #337ab7;
  text-decoration: none;
}
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
[role="button"] {
  cursor: pointer;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.text-center {
  text-align: center;
}
.text-justify {
  text-align: justify;
}
.text-nowrap {
  white-space: nowrap;
}
.text-lowercase {
  text-transform: lowercase;
}
.text-uppercase {
  text-transform: uppercase;
}
.text-capitalize {
  text-transform: capitalize;
}
.text-muted {
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
}
.col-xs-12 {
  width: 100%;
}
.col-xs-11 {
  width: 91.66666667%;
}
.col-xs-10 {
  width: 83.33333333%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-8 {
  width: 66.66666667%;
}
.col-xs-7 {
  width: 58.33333333%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-5 {
  width: 41.66666667%;
}
.col-xs-4 {
  width: 33.33333333%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-2 {
  width: 16.66666667%;
}
.col-xs-1 {
  width: 8.33333333%;
}
.col-xs-pull-12 {
  right: 100%;
}
.col-xs-pull-11 {
  right: 91.66666667%;
}
.col-xs-pull-10 {
  right: 83.33333333%;
}
.col-xs-pull-9 {
  right: 75%;
}
.col-xs-pull-8 {
  right: 66.66666667%;
}
.col-xs-pull-7 {
  right: 58.33333333%;
}
.col-xs-pull-6 {
  right: 50%;
}
.col-xs-pull-5 {
  right: 41.66666667%;
}
.col-xs-pull-4 {
  right: 33.33333333%;
}
.col-xs-pull-3 {
  right: 25%;
}
.col-xs-pull-2 {
  right: 16.66666667%;
}
.col-xs-pull-1 {
  right: 8.33333333%;
}
.col-xs-pull-0 {
  right: auto;
}
.col-xs-push-12 {
  left: 100%;
}
.col-xs-push-11 {
  left: 91.66666667%;
}
.col-xs-push-10 {
  left: 83.33333333%;
}
.col-xs-push-9 {
  left: 75%;
}
.col-xs-push-8 {
  left: 66.66666667%;
}
.col-xs-push-7 {
  left: 58.33333333%;
}
.col-xs-push-6 {
  left: 50%;
}
.col-xs-push-5 {
  left: 41.66666667%;
}
.col-xs-push-4 {
  left: 33.33333333%;
}
.col-xs-push-3 {
  left: 25%;
}
.col-xs-push-2 {
  left: 16.66666667%;
}
.col-xs-push-1 {
  left: 8.33333333%;
}
.col-xs-push-0 {
  left: auto;
}
.col-xs-offset-12 {
  margin-left: 100%;
}
.col-xs-offset-11 {
  margin-left: 91.66666667%;
}
.col-xs-offset-10 {
  margin-left: 83.33333333%;
}
.col-xs-offset-9 {
  margin-left: 75%;
}
.col-xs-offset-8 {
  margin-left: 66.66666667%;
}
.col-xs-offset-7 {
  margin-left: 58.33333333%;
}
.col-xs-offset-6 {
  margin-left: 50%;
}
.col-xs-offset-5 {
  margin-left: 41.66666667%;
}
.col-xs-offset-4 {
  margin-left: 33.33333333%;
}
.col-xs-offset-3 {
  margin-left: 25%;
}
.col-xs-offset-2 {
  margin-left: 16.66666667%;
}
.col-xs-offset-1 {
  margin-left: 8.33333333%;
}
.col-xs-offset-0 {
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
    float: left;
  }
  .col-sm-12 {
    width: 100%;
  }
  .col-sm-11 {
    width: 91.66666667%;
  }
  .col-sm-10 {
    width: 83.33333333%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-8 {
    width: 66.66666667%;
  }
  .col-sm-7 {
    width: 58.33333333%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-5 {
    width: 41.66666667%;
  }
  .col-sm-4 {
    width: 33.33333333%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-2 {
    width: 16.66666667%;
  }
  .col-sm-1 {
    width: 8.33333333%;
  }
  .col-sm-pull-12 {
    right: 100%;
  }
  .col-sm-pull-11 {
    right: 91.66666667%;
  }
  .col-sm-pull-10 {
    right: 83.33333333%;
  }
  .col-sm-pull-9 {
    right: 75%;
  }
  .col-sm-pull-8 {
    right: 66.66666667%;
  }
  .col-sm-pull-7 {
    right: 58.33333333%;
  }
  .col-sm-pull-6 {
    right: 50%;
  }
  .col-sm-pull-5 {
    right: 41.66666667%;
  }
  .col-sm-pull-4 {
    right: 33.33333333%;
  }
  .col-sm-pull-3 {
    right: 25%;
  }
  .col-sm-pull-2 {
    right: 16.66666667%;
  }
  .col-sm-pull-1 {
    right: 8.33333333%;
  }
  .col-sm-pull-0 {
    right: auto;
  }
  .col-sm-push-12 {
    left: 100%;
  }
  .col-sm-push-11 {
    left: 91.66666667%;
  }
  .col-sm-push-10 {
    left: 83.33333333%;
  }
  .col-sm-push-9 {
    left: 75%;
  }
  .col-sm-push-8 {
    left: 66.66666667%;
  }
  .col-sm-push-7 {
    left: 58.33333333%;
  }
  .col-sm-push-6 {
    left: 50%;
  }
  .col-sm-push-5 {
    left: 41.66666667%;
  }
  .col-sm-push-4 {
    left: 33.33333333%;
  }
  .col-sm-push-3 {
    left: 25%;
  }
  .col-sm-push-2 {
    left: 16.66666667%;
  }
  .col-sm-push-1 {
    left: 8.33333333%;
  }
  .col-sm-push-0 {
    left: auto;
  }
  .col-sm-offset-12 {
    margin-left: 100%;
  }
  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-sm-offset-9 {
    margin-left: 75%;
  }
  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-sm-offset-6 {
    margin-left: 50%;
  }
  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-sm-offset-3 {
    margin-left: 25%;
  }
  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-sm-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
    float: left;
  }
  .col-md-12 {
    width: 100%;
  }
  .col-md-11 {
    width: 91.66666667%;
  }
  .col-md-10 {
    width: 83.33333333%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-8 {
    width: 66.66666667%;
  }
  .col-md-7 {
    width: 58.33333333%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-5 {
    width: 41.66666667%;
  }
  .col-md-4 {
    width: 33.33333333%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-2 {
    width: 16.66666667%;
  }
  .col-md-1 {
    width: 8.33333333%;
  }
  .col-md-pull-12 {
    right: 100%;
  }
  .col-md-pull-11 {
    right: 91.66666667%;
  }
  .col-md-pull-10 {
    right: 83.33333333%;
  }
  .col-md-pull-9 {
    right: 75%;
  }
  .col-md-pull-8 {
    right: 66.66666667%;
  }
  .col-md-pull-7 {
    right: 58.33333333%;
  }
  .col-md-pull-6 {
    right: 50%;
  }
  .col-md-pull-5 {
    right: 41.66666667%;
  }
  .col-md-pull-4 {
    right: 33.33333333%;
  }
  .col-md-pull-3 {
    right: 25%;
  }
  .col-md-pull-2 {
    right: 16.66666667%;
  }
  .col-md-pull-1 {
    right: 8.33333333%;
  }
  .col-md-pull-0 {
    right: auto;
  }
  .col-md-push-12 {
    left: 100%;
  }
  .col-md-push-11 {
    left: 91.66666667%;
  }
  .col-md-push-10 {
    left: 83.33333333%;
  }
  .col-md-push-9 {
    left: 75%;
  }
  .col-md-push-8 {
    left: 66.66666667%;
  }
  .col-md-push-7 {
    left: 58.33333333%;
  }
  .col-md-push-6 {
    left: 50%;
  }
  .col-md-push-5 {
    left: 41.66666667%;
  }
  .col-md-push-4 {
    left: 33.33333333%;
  }
  .col-md-push-3 {
    left: 25%;
  }
  .col-md-push-2 {
    left: 16.66666667%;
  }
  .col-md-push-1 {
    left: 8.33333333%;
  }
  .col-md-push-0 {
    left: auto;
  }
  .col-md-offset-12 {
    margin-left: 100%;
  }
  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-md-offset-9 {
    margin-left: 75%;
  }
  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-md-offset-6 {
    margin-left: 50%;
  }
  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-md-offset-3 {
    margin-left: 25%;
  }
  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-md-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
    float: left;
  }
  .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
  .col-lg-10 {
    width: 83.33333333%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-8 {
    width: 66.66666667%;
  }
  .col-lg-7 {
    width: 58.33333333%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-5 {
    width: 41.66666667%;
  }
  .col-lg-4 {
    width: 33.33333333%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-2 {
    width: 16.66666667%;
  }
  .col-lg-1 {
    width: 8.33333333%;
  }
  .col-lg-pull-12 {
    right: 100%;
  }
  .col-lg-pull-11 {
    right: 91.66666667%;
  }
  .col-lg-pull-10 {
    right: 83.33333333%;
  }
  .col-lg-pull-9 {
    right: 75%;
  }
  .col-lg-pull-8 {
    right: 66.66666667%;
  }
  .col-lg-pull-7 {
    right: 58.33333333%;
  }
  .col-lg-pull-6 {
    right: 50%;
  }
  .col-lg-pull-5 {
    right: 41.66666667%;
  }
  .col-lg-pull-4 {
    right: 33.33333333%;
  }
  .col-lg-pull-3 {
    right: 25%;
  }
  .col-lg-pull-2 {
    right: 16.66666667%;
  }
  .col-lg-pull-1 {
    right: 8.33333333%;
  }
  .col-lg-pull-0 {
    right: auto;
  }
  .col-lg-push-12 {
    left: 100%;
  }
  .col-lg-push-11 {
    left: 91.66666667%;
  }
  .col-lg-push-10 {
    left: 83.33333333%;
  }
  .col-lg-push-9 {
    left: 75%;
  }
  .col-lg-push-8 {
    left: 66.66666667%;
  }
  .col-lg-push-7 {
    left: 58.33333333%;
  }
  .col-lg-push-6 {
    left: 50%;
  }
  .col-lg-push-5 {
    left: 41.66666667%;
  }
  .col-lg-push-4 {
    left: 33.33333333%;
  }
  .col-lg-push-3 {
    left: 25%;
  }
  .col-lg-push-2 {
    left: 16.66666667%;
  }
  .col-lg-push-1 {
    left: 8.33333333%;
  }
  .col-lg-push-0 {
    left: auto;
  }
  .col-lg-offset-12 {
    margin-left: 100%;
  }
  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-lg-offset-9 {
    margin-left: 75%;
  }
  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-lg-offset-6 {
    margin-left: 50%;
  }
  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-lg-offset-3 {
    margin-left: 25%;
  }
  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-lg-offset-0 {
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
}
input[type="file"] {
  display: block;
}
input[type="range"] {
  display: block;
  width: 100%;
}
select[multiple],
select[size] {
  height: auto;
}
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.form-control:-ms-input-placeholder {
  color: #999;
}
.form-control::-webkit-input-placeholder {
  color: #999;
}
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
}
.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}
.has-success .input-group-addon {
  color: #3c763d;
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
  color: #8a6d3b;
}
.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}
.has-warning .input-group-addon {
  color: #8a6d3b;
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}
.has-error .input-group-addon {
  color: #a94442;
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
}
a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}
.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
  background-color: #fff;
  border-color: #ccc;
}
.btn-default .badge {
  color: #fff;
  background-color: #333;
}
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}
.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
  width: 100%;
}
.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}
.fade.in {
  opacity: 1;
}
.collapse {
  display: none;
}
.collapse.in {
  display: block;
}
tr.collapse.in {
  display: table-row;
}
tbody.collapse.in {
  display: table-row-group;
}
.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
}
.dropdown-toggle:focus {
  outline: 0;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
  z-index: 2;
}
.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}
.btn-toolbar {
  margin-left: -5px;
}
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
}
.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}
.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}
.btn-group-vertical > .btn-group > .btn {
  float: none;
}
.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}
.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}
.input-group[class*="col-"] {
  float: none;
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}
.input-group-addon {
  padding: 6px 12px;
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.input-group-addon:last-child {
  border-left: 0;
}
.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}
.input-group-btn > .btn {
  position: relative;
}
.input-group-btn > .btn + .btn {
  margin-left: -1px;
}
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
  z-index: 2;
}
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}
.nav {
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.nav > li > a > img {
  max-width: none;
}
.nav-tabs {
  border-bottom: 1px solid #ddd;
}
.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}
.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.tab-content > .tab-pane {
  display: none;
}
.tab-content > .active {
  display: block;
}
.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
    box-shadow: none;
  }
  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }
  .navbar-collapse.in {
    overflow-y: visible;
  }
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
}
.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}
.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}
.navbar-brand {
  float: left;
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
}
.navbar-toggle:focus {
  outline: 0;
}
.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}
.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
  }
  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}
.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}
.navbar-default .navbar-brand {
  color: #777;
}
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
  background-color: #ddd;
}
.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}
.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}
.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #ccc;
    background-color: transparent;
  }
}
.navbar-default .navbar-link {
  color: #777;
}
.navbar-default .navbar-link:hover {
  color: #333;
}
.navbar-default .btn-link {
  color: #777;
}
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
  background-color: #333;
}
.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}
.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}
.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #444;
    background-color: transparent;
  }
}
.navbar-inverse .navbar-link {
  color: #9d9d9d;
}
.navbar-inverse .navbar-link:hover {
  color: #fff;
}
.navbar-inverse .btn-link {
  color: #9d9d9d;
}
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.pager .next > a,
.pager .next > span {
  float: right;
}
.pager .previous > a,
.pager .previous > span {
  float: left;
}
.pager .disabled > a,
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}
.list-group-item > .badge {
  float: right;
}
.list-group-item > .badge + .badge {
  margin-right: 5px;
}
.nav-pills > li > a > .badge {
  margin-left: 3px;
}
.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
}
.jumbotron .container {
  max-width: 100%;
}
@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }
  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
}
.alert > p,
.alert > ul {
  margin-bottom: 0;
}
.alert > p + p {
  margin-top: 5px;
}
.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}
.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
}
.alert-danger hr {
  border-top-color: #e4b9c0;
}
.alert-danger .alert-link {
  color: #843534;
}
@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
}
.media-object.img-thumbnail {
  max-width: none;
}
.media-right,
.media > .pull-right {
  padding-left: 10px;
}
.media-left,
.media > .pull-left {
  padding-right: 10px;
}
.media-left,
.media-right,
.media-body {
  display: table-cell;
  vertical-align: top;
}
.media-middle {
  vertical-align: middle;
}
.media-bottom {
  vertical-align: bottom;
}
.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.media-list {
  padding-left: 0;
  list-style: none;
}
.list-group {
  margin-bottom: 20px;
  padding-left: 0;
}
.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
.list-group-item:first-child {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
  color: #c7ddef;
}
.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}
a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}
a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}
.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}
a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}
a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}
.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}
a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}
a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}
.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}
a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}
a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
  border-top: 1px solid #ddd;
}
.panel-group .panel-footer {
  border-top: 0;
}
.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}
.panel-default {
  border-color: #ddd;
}
.panel-default > .panel-heading {
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
}
.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}
.panel-primary {
  border-color: #337ab7;
}
.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}
.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}
.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}
.panel-success {
  border-color: #d6e9c6;
}
.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}
.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}
.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}
.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}
.panel-info {
  border-color: #bce8f1;
}
.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}
.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}
.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}
.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}
.panel-warning {
  border-color: #faebcc;
}
.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}
.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}
.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}
.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}
.panel-danger {
  border-color: #ebccd1;
}
.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}
.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}
.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}
.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}
.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
  border: 0;
}
.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}
.embed-responsive-4by3 {
  padding-bottom: 75%;
}
.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
}
.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}
.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}
.modal-content {
  position: relative;
  background-color: #fff;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}
.modal-header .close {
  margin-top: -2px;
}
.modal-title {
  margin: 0;
  line-height: 1.42857143;
}
.modal-body {
  position: relative;
  padding: 15px;
}
.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}
.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0;
}
.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}
.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}
.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}
@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }
  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }
  .modal-sm {
    width: 300px;
  }
}
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
}
.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-left .tooltip-arrow {
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}
.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
.popover.top {
  margin-top: -10px;
}
.popover.right {
  margin-left: 10px;
}
.popover.bottom {
  margin-top: 10px;
}
.popover.left {
  margin-left: -10px;
}
.popover-title {
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
}
.popover-content {
  padding: 9px 14px;
}
.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
  }
}
.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}
.carousel-inner > .active {
  left: 0;
}
.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}
.carousel-inner > .next {
  left: 100%;
}
.carousel-inner > .prev {
  left: -100%;
}
.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}
.carousel-inner > .active.left {
  left: -100%;
}
.carousel-inner > .active.right {
  left: 100%;
}
.carousel-control {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.pull-right {
  float: right !important;
}
.pull-left {
  float: left !important;
}
.hide {
  display: none !important;
}
.show {
  display: block !important;
}
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
}
@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }
  table.visible-xs {
    display: table !important;
  }
  tr.visible-xs {
    display: table-row !important;
  }
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }
  table.visible-sm {
    display: table !important;
  }
  tr.visible-sm {
    display: table-row !important;
  }
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }
  table.visible-md {
    display: table !important;
  }
  tr.visible-md {
    display: table-row !important;
  }
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }
  table.visible-lg {
    display: table !important;
  }
  tr.visible-lg {
    display: table-row !important;
  }
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
  }
}
@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}
@media (min-width: 1200px) {
  .hidden-lg {
    display: none !important;
  }
}
.visible-print {
  display: none !important;
}
@media print {
  .visible-print {
    display: block !important;
  }
  table.visible-print {
    display: table !important;
  }
  tr.visible-print {
    display: table-row !important;
  }
  th.visible-print,
  td.visible-print {
    display: table-cell !important;
  }
}
.visible-print-block {
  display: none !important;
}
@media print {
  .visible-print-block {
    display: block !important;
  }
}
.visible-print-inline {
  display: none !important;
}
@media print {
  .visible-print-inline {
    display: inline !important;
  }
}
.visible-print-inline-block {
  display: none !important;
}
@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.7.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.7.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.7.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff2?v=4.7.0') format('woff2'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.7.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.7.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.7.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.fa-pull-left {
  float: left;
}
.fa-pull-right {
  float: right;
}
.fa.fa-pull-left {
  margin-right: .3em;
}
.fa.fa-pull-right {
  margin-left: .3em;
}
/* Deprecated as of 4.4.0 */
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
.fa-pulse {
  -webkit-animation: fa-spin 1s infinite steps(8);
  animation: fa-spin 1s infinite steps(8);
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=1)";
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2)";
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=3)";
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1)";
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1)";
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook-f:before,
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-feed:before,
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before,
.fa-gratipay:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper-pp:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-resistance:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-y-combinator-square:before,
.fa-yc-square:before,
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
.fa-buysellads:before {
  content: "\f20d";
}
.fa-connectdevelop:before {
  content: "\f20e";
}
.fa-dashcube:before {
  content: "\f210";
}
.fa-forumbee:before {
  content: "\f211";
}
.fa-leanpub:before {
  content: "\f212";
}
.fa-sellsy:before {
  content: "\f213";
}
.fa-shirtsinbulk:before {
  content: "\f214";
}
.fa-simplybuilt:before {
  content: "\f215";
}
.fa-skyatlas:before {
  content: "\f216";
}
.fa-cart-plus:before {
  content: "\f217";
}
.fa-cart-arrow-down:before {
  content: "\f218";
}
.fa-diamond:before {
  content: "\f219";
}
.fa-ship:before {
  content: "\f21a";
}
.fa-user-secret:before {
  content: "\f21b";
}
.fa-motorcycle:before {
  content: "\f21c";
}
.fa-street-view:before {
  content: "\f21d";
}
.fa-heartbeat:before {
  content: "\f21e";
}
.fa-venus:before {
  content: "\f221";
}
.fa-mars:before {
  content: "\f222";
}
.fa-mercury:before {
  content: "\f223";
}
.fa-intersex:before,
.fa-transgender:before {
  content: "\f224";
}
.fa-transgender-alt:before {
  content: "\f225";
}
.fa-venus-double:before {
  content: "\f226";
}
.fa-mars-double:before {
  content: "\f227";
}
.fa-venus-mars:before {
  content: "\f228";
}
.fa-mars-stroke:before {
  content: "\f229";
}
.fa-mars-stroke-v:before {
  content: "\f22a";
}
.fa-mars-stroke-h:before {
  content: "\f22b";
}
.fa-neuter:before {
  content: "\f22c";
}
.fa-genderless:before {
  content: "\f22d";
}
.fa-facebook-official:before {
  content: "\f230";
}
.fa-pinterest-p:before {
  content: "\f231";
}
.fa-whatsapp:before {
  content: "\f232";
}
.fa-server:before {
  content: "\f233";
}
.fa-user-plus:before {
  content: "\f234";
}
.fa-user-times:before {
  content: "\f235";
}
.fa-hotel:before,
.fa-bed:before {
  content: "\f236";
}
.fa-viacoin:before {
  content: "\f237";
}
.fa-train:before {
  content: "\f238";
}
.fa-subway:before {
  content: "\f239";
}
.fa-medium:before {
  content: "\f23a";
}
.fa-yc:before,
.fa-y-combinator:before {
  content: "\f23b";
}
.fa-optin-monster:before {
  content: "\f23c";
}
.fa-opencart:before {
  content: "\f23d";
}
.fa-expeditedssl:before {
  content: "\f23e";
}
.fa-battery-4:before,
.fa-battery:before,
.fa-battery-full:before {
  content: "\f240";
}
.fa-battery-3:before,
.fa-battery-three-quarters:before {
  content: "\f241";
}
.fa-battery-2:before,
.fa-battery-half:before {
  content: "\f242";
}
.fa-battery-1:before,
.fa-battery-quarter:before {
  content: "\f243";
}
.fa-battery-0:before,
.fa-battery-empty:before {
  content: "\f244";
}
.fa-mouse-pointer:before {
  content: "\f245";
}
.fa-i-cursor:before {
  content: "\f246";
}
.fa-object-group:before {
  content: "\f247";
}
.fa-object-ungroup:before {
  content: "\f248";
}
.fa-sticky-note:before {
  content: "\f249";
}
.fa-sticky-note-o:before {
  content: "\f24a";
}
.fa-cc-jcb:before {
  content: "\f24b";
}
.fa-cc-diners-club:before {
  content: "\f24c";
}
.fa-clone:before {
  content: "\f24d";
}
.fa-balance-scale:before {
  content: "\f24e";
}
.fa-hourglass-o:before {
  content: "\f250";
}
.fa-hourglass-1:before,
.fa-hourglass-start:before {
  content: "\f251";
}
.fa-hourglass-2:before,
.fa-hourglass-half:before {
  content: "\f252";
}
.fa-hourglass-3:before,
.fa-hourglass-end:before {
  content: "\f253";
}
.fa-hourglass:before {
  content: "\f254";
}
.fa-hand-grab-o:before,
.fa-hand-rock-o:before {
  content: "\f255";
}
.fa-hand-stop-o:before,
.fa-hand-paper-o:before {
  content: "\f256";
}
.fa-hand-scissors-o:before {
  content: "\f257";
}
.fa-hand-lizard-o:before {
  content: "\f258";
}
.fa-hand-spock-o:before {
  content: "\f259";
}
.fa-hand-pointer-o:before {
  content: "\f25a";
}
.fa-hand-peace-o:before {
  content: "\f25b";
}
.fa-trademark:before {
  content: "\f25c";
}
.fa-registered:before {
  content: "\f25d";
}
.fa-creative-commons:before {
  content: "\f25e";
}
.fa-gg:before {
  content: "\f260";
}
.fa-gg-circle:before {
  content: "\f261";
}
.fa-tripadvisor:before {
  content: "\f262";
}
.fa-odnoklassniki:before {
  content: "\f263";
}
.fa-odnoklassniki-square:before {
  content: "\f264";
}
.fa-get-pocket:before {
  content: "\f265";
}
.fa-wikipedia-w:before {
  content: "\f266";
}
.fa-safari:before {
  content: "\f267";
}
.fa-chrome:before {
  content: "\f268";
}
.fa-firefox:before {
  content: "\f269";
}
.fa-opera:before {
  content: "\f26a";
}
.fa-internet-explorer:before {
  content: "\f26b";
}
.fa-tv:before,
.fa-television:before {
  content: "\f26c";
}
.fa-contao:before {
  content: "\f26d";
}
.fa-500px:before {
  content: "\f26e";
}
.fa-amazon:before {
  content: "\f270";
}
.fa-calendar-plus-o:before {
  content: "\f271";
}
.fa-calendar-minus-o:before {
  content: "\f272";
}
.fa-calendar-times-o:before {
  content: "\f273";
}
.fa-calendar-check-o:before {
  content: "\f274";
}
.fa-industry:before {
  content: "\f275";
}
.fa-map-pin:before {
  content: "\f276";
}
.fa-map-signs:before {
  content: "\f277";
}
.fa-map-o:before {
  content: "\f278";
}
.fa-map:before {
  content: "\f279";
}
.fa-commenting:before {
  content: "\f27a";
}
.fa-commenting-o:before {
  content: "\f27b";
}
.fa-houzz:before {
  content: "\f27c";
}
.fa-vimeo:before {
  content: "\f27d";
}
.fa-black-tie:before {
  content: "\f27e";
}
.fa-fonticons:before {
  content: "\f280";
}
.fa-reddit-alien:before {
  content: "\f281";
}
.fa-edge:before {
  content: "\f282";
}
.fa-credit-card-alt:before {
  content: "\f283";
}
.fa-codiepie:before {
  content: "\f284";
}
.fa-modx:before {
  content: "\f285";
}
.fa-fort-awesome:before {
  content: "\f286";
}
.fa-usb:before {
  content: "\f287";
}
.fa-product-hunt:before {
  content: "\f288";
}
.fa-mixcloud:before {
  content: "\f289";
}
.fa-scribd:before {
  content: "\f28a";
}
.fa-pause-circle:before {
  content: "\f28b";
}
.fa-pause-circle-o:before {
  content: "\f28c";
}
.fa-stop-circle:before {
  content: "\f28d";
}
.fa-stop-circle-o:before {
  content: "\f28e";
}
.fa-shopping-bag:before {
  content: "\f290";
}
.fa-shopping-basket:before {
  content: "\f291";
}
.fa-hashtag:before {
  content: "\f292";
}
.fa-bluetooth:before {
  content: "\f293";
}
.fa-bluetooth-b:before {
  content: "\f294";
}
.fa-percent:before {
  content: "\f295";
}
.fa-gitlab:before {
  content: "\f296";
}
.fa-wpbeginner:before {
  content: "\f297";
}
.fa-wpforms:before {
  content: "\f298";
}
.fa-envira:before {
  content: "\f299";
}
.fa-universal-access:before {
  content: "\f29a";
}
.fa-wheelchair-alt:before {
  content: "\f29b";
}
.fa-question-circle-o:before {
  content: "\f29c";
}
.fa-blind:before {
  content: "\f29d";
}
.fa-audio-description:before {
  content: "\f29e";
}
.fa-volume-control-phone:before {
  content: "\f2a0";
}
.fa-braille:before {
  content: "\f2a1";
}
.fa-assistive-listening-systems:before {
  content: "\f2a2";
}
.fa-asl-interpreting:before,
.fa-american-sign-language-interpreting:before {
  content: "\f2a3";
}
.fa-deafness:before,
.fa-hard-of-hearing:before,
.fa-deaf:before {
  content: "\f2a4";
}
.fa-glide:before {
  content: "\f2a5";
}
.fa-glide-g:before {
  content: "\f2a6";
}
.fa-signing:before,
.fa-sign-language:before {
  content: "\f2a7";
}
.fa-low-vision:before {
  content: "\f2a8";
}
.fa-viadeo:before {
  content: "\f2a9";
}
.fa-viadeo-square:before {
  content: "\f2aa";
}
.fa-snapchat:before {
  content: "\f2ab";
}
.fa-snapchat-ghost:before {
  content: "\f2ac";
}
.fa-snapchat-square:before {
  content: "\f2ad";
}
.fa-pied-piper:before {
  content: "\f2ae";
}
.fa-first-order:before {
  content: "\f2b0";
}
.fa-yoast:before {
  content: "\f2b1";
}
.fa-themeisle:before {
  content: "\f2b2";
}
.fa-google-plus-circle:before,
.fa-google-plus-official:before {
  content: "\f2b3";
}
.fa-fa:before,
.fa-font-awesome:before {
  content: "\f2b4";
}
.fa-handshake-o:before {
  content: "\f2b5";
}
.fa-envelope-open:before {
  content: "\f2b6";
}
.fa-envelope-open-o:before {
  content: "\f2b7";
}
.fa-linode:before {
  content: "\f2b8";
}
.fa-address-book:before {
  content: "\f2b9";
}
.fa-address-book-o:before {
  content: "\f2ba";
}
.fa-vcard:before,
.fa-address-card:before {
  content: "\f2bb";
}
.fa-vcard-o:before,
.fa-address-card-o:before {
  content: "\f2bc";
}
.fa-user-circle:before {
  content: "\f2bd";
}
.fa-user-circle-o:before {
  content: "\f2be";
}
.fa-user-o:before {
  content: "\f2c0";
}
.fa-id-badge:before {
  content: "\f2c1";
}
.fa-drivers-license:before,
.fa-id-card:before {
  content: "\f2c2";
}
.fa-drivers-license-o:before,
.fa-id-card-o:before {
  content: "\f2c3";
}
.fa-quora:before {
  content: "\f2c4";
}
.fa-free-code-camp:before {
  content: "\f2c5";
}
.fa-telegram:before {
  content: "\f2c6";
}
.fa-thermometer-4:before,
.fa-thermometer:before,
.fa-thermometer-full:before {
  content: "\f2c7";
}
.fa-thermometer-3:before,
.fa-thermometer-three-quarters:before {
  content: "\f2c8";
}
.fa-thermometer-2:before,
.fa-thermometer-half:before {
  content: "\f2c9";
}
.fa-thermometer-1:before,
.fa-thermometer-quarter:before {
  content: "\f2ca";
}
.fa-thermometer-0:before,
.fa-thermometer-empty:before {
  content: "\f2cb";
}
.fa-shower:before {
  content: "\f2cc";
}
.fa-bathtub:before,
.fa-s15:before,
.fa-bath:before {
  content: "\f2cd";
}
.fa-podcast:before {
  content: "\f2ce";
}
.fa-window-maximize:before {
  content: "\f2d0";
}
.fa-window-minimize:before {
  content: "\f2d1";
}
.fa-window-restore:before {
  content: "\f2d2";
}
.fa-times-rectangle:before,
.fa-window-close:before {
  content: "\f2d3";
}
.fa-times-rectangle-o:before,
.fa-window-close-o:before {
  content: "\f2d4";
}
.fa-bandcamp:before {
  content: "\f2d5";
}
.fa-grav:before {
  content: "\f2d6";
}
.fa-etsy:before {
  content: "\f2d7";
}
.fa-imdb:before {
  content: "\f2d8";
}
.fa-ravelry:before {
  content: "\f2d9";
}
.fa-eercast:before {
  content: "\f2da";
}
.fa-microchip:before {
  content: "\f2db";
}
.fa-snowflake-o:before {
  content: "\f2dc";
}
.fa-superpowers:before {
  content: "\f2dd";
}
.fa-wpexplorer:before {
  content: "\f2de";
}
.fa-meetup:before {
  content: "\f2e0";
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box 
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this 
new spec completely include:

    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+ 
    Opera 17.0+

Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
div.traceback-wrapper pre.traceback {
  max-height: 600px;
  overflow: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 5px;
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
[dir="rtl"] #ipython_notebook {
  margin-right: 10px;
  margin-left: 0;
}
[dir="rtl"] #ipython_notebook.pull-left {
  float: right !important;
  float: right;
}
.flex-spacer {
  flex: 1;
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#kernel_logo_widget {
  margin: 0 10px;
}
span#login_widget {
  float: right;
}
[dir="rtl"] span#login_widget {
  float: left;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
.modal-header {
  cursor: move;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
[dir="rtl"] .center-nav form.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] .center-nav .navbar-text {
  float: right;
}
[dir="rtl"] .navbar-inner {
  text-align: right;
}
[dir="rtl"] div.text-left {
  text-align: right;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  position: absolute;
  display: block;
  width: 100%;
  height: 100%;
  overflow: hidden;
  cursor: pointer;
  opacity: 0;
  z-index: 2;
}
.alternate_upload .btn-xs > input.fileinput {
  margin: -1px -5px;
}
.alternate_upload .btn-upload {
  position: relative;
  height: 22px;
}
::-webkit-file-upload-button {
  cursor: pointer;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
ul#tabs {
  margin-bottom: 4px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
[dir="rtl"] ul#tabs.nav-tabs > li {
  float: right;
}
[dir="rtl"] ul#tabs.nav.nav-tabs {
  padding-right: 0;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
[dir="rtl"] .list_toolbar .tree-buttons .pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .list_toolbar .col-sm-4,
[dir="rtl"] .list_toolbar .col-sm-8 {
  float: right;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: text-bottom;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
[dir="rtl"] .list_item > div input {
  margin-right: 0;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_modified {
  margin-right: 7px;
  margin-left: 7px;
}
[dir="rtl"] .item_modified.pull-right {
  float: left !important;
  float: left;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
[dir="rtl"] .item_buttons.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .item_buttons .kernel-name {
  margin-left: 7px;
  float: right;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
.sort_button {
  display: inline-block;
  padding-left: 7px;
}
[dir="rtl"] .sort_button.pull-right {
  float: left !important;
  float: left;
}
#tree-selector {
  padding-right: 0px;
}
#button-select-all {
  min-width: 50px;
}
[dir="rtl"] #button-select-all.btn {
  float: right ;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
  margin-top: 2px;
  height: 16px;
}
[dir="rtl"] #select-all.pull-left {
  float: right !important;
  float: right;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.fa-pull-left {
  margin-right: .3em;
}
.folder_icon:before.fa-pull-right {
  margin-left: .3em;
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.fa-pull-left {
  margin-right: .3em;
}
.file_icon:before.fa-pull-right {
  margin-left: .3em;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
#new-menu .dropdown-header {
  font-size: 10px;
  border-bottom: 1px solid #e5e5e5;
  padding: 0 0 3px;
  margin: -3px 20px 0;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.move-button {
  display: none;
}
.download-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
.CodeMirror-dialog {
  background-color: #fff;
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI escape sequences */
/* The color values are a mix of
   http://www.xcolors.net/dl/baskerville-ivorylight and
   http://www.xcolors.net/dl/euphrasia */
.ansi-black-fg {
  color: #3E424D;
}
.ansi-black-bg {
  background-color: #3E424D;
}
.ansi-black-intense-fg {
  color: #282C36;
}
.ansi-black-intense-bg {
  background-color: #282C36;
}
.ansi-red-fg {
  color: #E75C58;
}
.ansi-red-bg {
  background-color: #E75C58;
}
.ansi-red-intense-fg {
  color: #B22B31;
}
.ansi-red-intense-bg {
  background-color: #B22B31;
}
.ansi-green-fg {
  color: #00A250;
}
.ansi-green-bg {
  background-color: #00A250;
}
.ansi-green-intense-fg {
  color: #007427;
}
.ansi-green-intense-bg {
  background-color: #007427;
}
.ansi-yellow-fg {
  color: #DDB62B;
}
.ansi-yellow-bg {
  background-color: #DDB62B;
}
.ansi-yellow-intense-fg {
  color: #B27D12;
}
.ansi-yellow-intense-bg {
  background-color: #B27D12;
}
.ansi-blue-fg {
  color: #208FFB;
}
.ansi-blue-bg {
  background-color: #208FFB;
}
.ansi-blue-intense-fg {
  color: #0065CA;
}
.ansi-blue-intense-bg {
  background-color: #0065CA;
}
.ansi-magenta-fg {
  color: #D160C4;
}
.ansi-magenta-bg {
  background-color: #D160C4;
}
.ansi-magenta-intense-fg {
  color: #A03196;
}
.ansi-magenta-intense-bg {
  background-color: #A03196;
}
.ansi-cyan-fg {
  color: #60C6C8;
}
.ansi-cyan-bg {
  background-color: #60C6C8;
}
.ansi-cyan-intense-fg {
  color: #258F8F;
}
.ansi-cyan-intense-bg {
  background-color: #258F8F;
}
.ansi-white-fg {
  color: #C5C1B4;
}
.ansi-white-bg {
  background-color: #C5C1B4;
}
.ansi-white-intense-fg {
  color: #A1A6B2;
}
.ansi-white-intense-bg {
  background-color: #A1A6B2;
}
.ansi-default-inverse-fg {
  color: #FFFFFF;
}
.ansi-default-inverse-bg {
  background-color: #000000;
}
.ansi-bold {
  font-weight: bold;
}
.ansi-underline {
  text-decoration: underline;
}
/* The following styles are deprecated an will be removed in a future version */
.ansibold {
  font-weight: bold;
}
.ansi-inverse {
  outline: 0.5px dotted;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  position: relative;
  overflow: visible;
}
div.cell:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: transparent;
}
div.cell.jupyter-soft-selected {
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected,
div.cell.selected.jupyter-soft-selected {
  border-color: #ababab;
}
div.cell.selected:before,
div.cell.selected.jupyter-soft-selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #42A5F5;
}
@media print {
  div.cell.selected,
  div.cell.selected.jupyter-soft-selected {
    border-color: transparent;
  }
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
}
.edit_mode div.cell.selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #66BB6A;
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  /* Note that this should set vertical padding only, since CodeMirror assumes
       that horizontal padding will be set on CodeMirror pre */
  padding: 0.4em 0;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. This sets horizontal padding only,
    use .CodeMirror-lines for vertical */
  padding: 0 0.4em;
  border: 0;
  border-radius: 0;
}
.CodeMirror-cursor {
  border-left: 1.4px solid black;
}
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .CodeMirror-cursor {
    border-left: 2px solid black;
  }
}
@media screen and (min-width: 4320px) {
  .CodeMirror-cursor {
    border-left: 4px solid black;
  }
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
div.output_area .mglyph > img {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 1px 0 1px 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul:not(.list-inline),
.rendered_html ol:not(.list-inline) {
  padding-left: 2em;
}
.rendered_html ul {
  list-style: disc;
}
.rendered_html ul ul {
  list-style: square;
  margin-top: 0;
}
.rendered_html ul ul ul {
  list-style: circle;
}
.rendered_html ol {
  list-style: decimal;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin-top: 0;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
  padding: 0px;
  background-color: #fff;
}
.rendered_html code {
  background-color: #eff0f1;
}
.rendered_html p code {
  padding: 1px 5px;
}
.rendered_html pre code {
  background-color: #fff;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  color: #000;
  font-size: 100%;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: none;
  border-collapse: collapse;
  border-spacing: 0;
  color: black;
  font-size: 12px;
  table-layout: fixed;
}
.rendered_html thead {
  border-bottom: 1px solid black;
  vertical-align: bottom;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  text-align: right;
  vertical-align: middle;
  padding: 0.5em 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html tbody tr:nth-child(odd) {
  background: #f5f5f5;
}
.rendered_html tbody tr:hover {
  background: rgba(66, 165, 245, 0.2);
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
.rendered_html .alert {
  margin-bottom: initial;
}
.rendered_html * + .alert {
  margin-top: 1em;
}
[dir="rtl"] .rendered_html p {
  text-align: right;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.rendered .rendered_html tr,
.text_cell.rendered .rendered_html th,
.text_cell.rendered .rendered_html td {
  max-width: none;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.text_cell .dropzone .input_area {
  border: 2px dashed #bababa;
  margin: -1px;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
.jupyter-keybindings {
  padding: 1px;
  line-height: 24px;
  border-bottom: 1px solid gray;
}
.jupyter-keybindings input {
  margin: 0;
  padding: 0;
  border: none;
}
.jupyter-keybindings i {
  padding: 6px;
}
.well code {
  background-color: #ffffff;
  border-color: #ababab;
  border-width: 1px;
  border-style: solid;
  padding: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.tags_button_container {
  width: 100%;
  display: flex;
}
.tag-container {
  display: flex;
  flex-direction: row;
  flex-grow: 1;
  overflow: hidden;
  position: relative;
}
.tag-container > * {
  margin: 0 4px;
}
.remove-tag-btn {
  margin-left: 4px;
}
.tags-input {
  display: flex;
}
.cell-tag:last-child:after {
  content: "";
  position: absolute;
  right: 0;
  width: 40px;
  height: 100%;
  /* Fade to background color of cell toolbar */
  background: linear-gradient(to right, rgba(0, 0, 0, 0), #EEE);
}
.tags-input > * {
  margin-left: 4px;
}
.cell-tag,
.tags-input input,
.tags-input button {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  box-shadow: none;
  width: inherit;
  font-size: inherit;
  height: 22px;
  line-height: 22px;
  padding: 0px 4px;
  display: inline-block;
}
.cell-tag:focus,
.tags-input input:focus,
.tags-input button:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.cell-tag::-moz-placeholder,
.tags-input input::-moz-placeholder,
.tags-input button::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.cell-tag:-ms-input-placeholder,
.tags-input input:-ms-input-placeholder,
.tags-input button:-ms-input-placeholder {
  color: #999;
}
.cell-tag::-webkit-input-placeholder,
.tags-input input::-webkit-input-placeholder,
.tags-input button::-webkit-input-placeholder {
  color: #999;
}
.cell-tag::-ms-expand,
.tags-input input::-ms-expand,
.tags-input button::-ms-expand {
  border: 0;
  background-color: transparent;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
.cell-tag[readonly],
.tags-input input[readonly],
.tags-input button[readonly],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  background-color: #eeeeee;
  opacity: 1;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  cursor: not-allowed;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button {
  height: auto;
}
select.cell-tag,
select.tags-input input,
select.tags-input button {
  height: 30px;
  line-height: 30px;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button,
select[multiple].cell-tag,
select[multiple].tags-input input,
select[multiple].tags-input button {
  height: auto;
}
.cell-tag,
.tags-input button {
  padding: 0px 4px;
}
.cell-tag {
  background-color: #fff;
  white-space: nowrap;
}
.tags-input input[type=text]:focus {
  outline: none;
  box-shadow: none;
  border-color: #ccc;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
[dir="rtl"] #kernel_logo_widget {
  float: left !important;
  float: left;
}
.modal .modal-body .move-path {
  display: flex;
  flex-direction: row;
  justify-content: space;
  align-items: center;
}
.modal .modal-body .move-path .server-root {
  padding-right: 20px;
}
.modal .modal-body .move-path .path-input {
  flex: 1;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
[dir="rtl"] #menubar .navbar-toggle {
  float: right;
}
[dir="rtl"] #menubar .navbar-collapse {
  clear: right;
}
[dir="rtl"] #menubar .navbar-nav {
  float: right;
}
[dir="rtl"] #menubar .nav {
  padding-right: 0px;
}
[dir="rtl"] #menubar .navbar-nav > li {
  float: right;
}
[dir="rtl"] #menubar .navbar-right {
  float: left !important;
}
[dir="rtl"] ul.dropdown-menu {
  text-align: right;
  left: auto;
}
[dir="rtl"] ul#new-menu.dropdown-menu {
  right: auto;
  left: 0;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
[dir="rtl"] i.menu-icon.pull-right {
  float: left !important;
  float: left;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
[dir="rtl"] ul#help_menu li a {
  padding-left: 2.2em;
}
[dir="rtl"] ul#help_menu li a i {
  margin-right: 0;
  margin-left: -1.2em;
}
[dir="rtl"] ul#help_menu li a i.pull-right {
  float: left !important;
  float: left;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
[dir="rtl"] .dropdown-submenu > .dropdown-menu {
  right: 100%;
  margin-right: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.fa-pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.fa-pull-right {
  margin-left: .3em;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
[dir="rtl"] .dropdown-submenu > a:after {
  float: left;
  content: "\f0d9";
  margin-right: 0;
  margin-left: -10px;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
[dir="rtl"] #notification_area {
  float: left !important;
  float: left;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] .indicator_area {
  float: left !important;
  float: left;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
[dir="rtl"] #kernel_indicator {
  float: left !important;
  float: left;
  border-left: 0;
  border-right: 1px solid;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] #modal_indicator {
  float: left !important;
  float: left;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for 
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 21ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  height: 30px;
  margin-top: 4px;
  display: flex;
  justify-content: flex-start;
  align-items: baseline;
  width: 50%;
  flex: 1;
}
span.save_widget span.filename {
  height: 100%;
  line-height: 1em;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  text-overflow: ellipsis;
  overflow: hidden;
  white-space: nowrap;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
[dir="rtl"] span.save_widget.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] span.save_widget span.filename {
  margin-left: 0;
  margin-right: 16px;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
  white-space: nowrap;
  padding: 0 5px;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
    padding: 0 0 0 5px;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
.toolbar-btn-label {
  margin-left: 6px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
[dir="rtl"] .btn-group > .btn,
.btn-group-vertical > .btn {
  float: right;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
[dir="rtl"] ul.typeahead-list i {
  margin-left: 0;
  margin-right: -10px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
ul.typeahead-list  > li > a.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .typeahead-list {
  text-align: right;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  min-width: 20px;
  color: transparent;
}
[dir="rtl"] .no-shortcut.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .command-shortcut.pull-right {
  float: left !important;
  float: left;
}
.command-shortcut:before {
  content: "(command mode)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
[dir="rtl"] .edit-shortcut.pull-right {
  float: left !important;
  float: left;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
[dir="ltr"] #find-and-replace .input-group-btn + .form-control {
  border-left: none;
}
[dir="rtl"] #find-and-replace .input-group-btn + .form-control {
  border-right: none;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  width: 100%;
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal .xterm-rows {
  padding: 10px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/latest.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-python"><pre><span></span><span class="c1"># Bar plot</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>

<span class="c1"># Load the tips dataset</span>
<span class="n">tips</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">load_dataset</span><span class="p">(</span><span class="s2">&quot;tips&quot;</span><span class="p">)</span>

<span class="c1"># Plot the total bill amount for each day</span>
<span class="n">sns</span><span class="o">.</span><span class="n">barplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s2">&quot;day&quot;</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="s2">&quot;total_bill&quot;</span><span class="p">,</span> <span class="n">data</span><span class="o">=</span><span class="n">tips</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[&nbsp;]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.axes._subplots.AxesSubplot at 0x7fb349d43910&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAYUAAAEMCAYAAAArnKpYAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADh0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uMy4yLjIsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy+WH4yJAAAUNElEQVR4nO3de1BU98HG8We57HpBBAz4YmPj5dWEprEUieh0nChOixoUsdNiodUwTWuMk0stpU5wQIkzFrWxMUVN8ra+Y2pjk1HDJVqdaYyd6SSjvLaZWqMSg6mKYlBRo+G2e94/0vwqjeACyzkLfD//LJzdPfvsGeKT37n8jsuyLEsAAEgKcToAACB4UAoAAINSAAAYlAIAwKAUAAAGpQAAMCgFAIAR5nSAQLhy5YZ8Pi63AAB/hIS4FB09+LbP9YlS8PksSgEAAoDdRwAAg1IAABiUAgDAoBQAAAalAAAwKAUAgEEpAECAHDlSpVWrCnTkSJXTUbqsT1ynAADB4PXXf6+amg/V2PipkpKSnY7TJYwUACBAPv20sc1jb0QpAAAMSgEAYFAKAACDUgAAGJQCAMCgFAAABqUAADAoBaAf6wtX4CKwuKIZ6Mf6whW4CCxGCkA/1heuwEVgUQoAAINSAAAYlAIAwKAUAAAGpQAAMCgFAIDBdQoA+oSoIW6FD/A4miE01GUeY2OHOJajpbFJDdebu/ReSgFAnxA+wKM9C3MdzXDzQp15dDLL7G1bpS6WAruPAAAGpQAAMCgFAIBBKaBXYVZPoGdxoBm9CrN6Aj2LkQJ6FWb1BHoWpQAAMGzZfXTlyhXl5+frn//8p9xut+655x4VFxcrJiZGf/vb31RYWKimpiZ96Utf0rp16zRs2DA7YgGOihzqkcftdjRDsFxs1dTcrGtXmxz7fPybLaXgcrn06KOPKiUlRZJUUlKi9evXa/Xq1frZz36mNWvWKDk5WZs2bdL69eu1Zs0aO2IBjvK43Xpk61OOZqi79rF5dDLL/+Y+L4lSCAa27D6KiooyhSBJiYmJqq2t1dGjR+XxeJSc/NkBwwULFuiPf/yjHZEAALdh+zEFn8+nV199VampqTp//rxGjBhhnouJiZHP51NDQ4PdsQAAcqAUnn32WQ0aNEjf//737f5oAMAd2HqdQklJiT766CNt2bJFISEhio+PV21trXn+8uXLCgkJUVRUlJ2xAAD/YttI4bnnntPRo0dVWloq97/OuPjqV7+qxsZGVVV9dnXqjh07NHPmTLsi2YarcAH0FraMFKqrq/Xiiy9q1KhRWrBggSTp7rvvVmlpqdauXauioqI2p6T2NVyFC6C3sKUUxo0bpxMnTtz2uaSkJFVUVNgRwzFchQv0D+EhLsn7r8deiiuaASBAvhEZpZFuj74R2XuPizIhHgAEyJgBAzVmwECnY3QLIwUAgEEpAAAMSgEAYFAKAACDUgAAGJQC0I+5wkPaPAL8JQD92NAJw+UZPlhDJwx3OgqCBNcpAP3YwLuHaODdzt1xDcGHkQIAwKAUAAAGpQAAMCgFAIBBKQAAjD5/9tGQyAEa4Al3NENoqMs8xsY6d6ZHY1OLrl/jng4A2tfnS2GAJ1zZ+dsdzVBff12SdKH+uqNZfr82R9dFKQBoH7uPAAAGpQAAMCgFAIDR548pILCih7oV5vY49vnBctBeklqbm3TlarOjGYBAoxTQKWFuj/5v7aOOfX7TlTrz6GQOSZqY/z+SKAX0Lew+AgAYlAIAwKAUAAAGpQAAMCgFAIBBKQAADEoBAGBQCgAAg1IAABiUgg1coeFtHgEgWFEKNogYkaTwiP9SxIgkp6MAQIeY+8gGnqEj5Rk60ukYAHBHjBQAAIZtI4WSkhLt27dP586dU0VFhcaPHy9JSk1Nldvtlsfz2XTMeXl5mjp1ql2xAAC3sK0UZsyYoYULFyonJ+cLz23cuNGUBADAObaVQnJysl0fBQDooqA40JyXlyfLsjRx4kQtW7ZMkZGRTkcCgH7J8QPN27dvV3l5uXbu3CnLslRcXOx0JADotzocKbzzzjt+rWTKlCldDhAfHy9Jcrvdys7O1pIlS7q8LgBA93RYCgUFBXdcgcvl0p/+9KcuffjNmzfl9Xo1ZMgQWZalPXv2KCEhoUvrAgB0X4el8NZbbwXsg1avXq39+/ervr5eubm5ioqK0pYtW/TEE0/I6/XK5/Np7NixKioqCthnAgA6x7YDzStWrNCKFSu+sPyNN96wKwIA4A46LIWHHnpILpfrjit5++23A5UHAOCgDkth3bp1duUAAASBDkth0qRJduUAAASBDkth8+bN5hTR559/vt3XPfXUU4FNBQBwRIelcOHChdv+DADomzoshVWrVpmf16xZ0+NhAADO6tQpqadPn9bevXt18eJFxcXFadasWRo1alQPRQMA2M3vuY8qKiqUmZmpEydOaODAgTp58qQyMzNVUVHRk/mANjxhIW0eAQSW3yOFX/3qV3rppZf04IMPmmVVVVXKz8/XnDlzeiQc8J++9d/ROlhzVQ+NHup0FKBP8rsUbty4ocTExDbLvva1r+nmzZsBDwW0JyF2kBJiBzkdA+iz/B6D5+bm6rnnnlNTU5MkqbGxURs2bFBubm6PhQMA2MvvaS4sy1J9fb1eeeUVRUZG6tq1a7IsS7GxsVq8eLEtYQEAPYtpLgAARkCnufjxj3+sl156qVuBAADOCeh5fVVVVYFcHQDAZpzsDQAwKAUAgEEpAACMgJaCZVmBXB0AwGYBLYXHHnsskKsDANisw1NSO7qxzq0+v8kOF7EBQO/m9012AAB9X4elwI11AKB/6dRNdiTpk08+0ZUrV9osGzlyZMACAQCc43cpfPDBB8rLy9Px48flcrlkWZaZLO/999/vsYAAAPv4ffbRqlWrlJKSokOHDikiIkKHDx9WVlaWfvGLX/RkPgCAjfwuhePHjysvL0+RkZGyLEtDhgxRfn6+32coAQCCn9+l4PF41NraKkmKjo5WbW2tfD6fGhoaeiwcAMBefh9TmDhxovbu3av58+crLS1NP/rRj+R2uzV58uSezAcAsJHfpXDrbqJly5Zp3LhxunHjhjIzM3skGADAfn7vPvrNb37z7zeFhCgjI0PZ2dnasWNHjwQDANjP71IoLS297fLNmzcHLAwAwFl33H30zjvvSJJ8Pp/efffdNjOhnj17VoMHD+65dAAAW92xFAoKCiRJTU1NeuaZZ8xyl8ul2NhYrVixoufSAQBsdcdSeOuttyRJ+fn5Wrt2bY8HAgA4x+9jCmvXrlVra6sOHz6syspKVVVVmesW7qSkpESpqam69957dfLkSbO8pqZGWVlZSktLU1ZWlk6fPt3pLwAACBy/T0n98MMP9dhjj6mxsVHx8fE6f/68PB6PtmzZorFjx3b43hkzZmjhwoXKyclps7yoqEjZ2dnKyMhQWVmZCgsLtW3btq59EwBAt/k9Uli5cqW++93v6uDBg/rDH/6gP//5z1qwYIFWrlx5x/cmJycrPj6+zbJLly7p2LFjSk9PlySlp6fr2LFjunz5cue+AQAgYDo191Fubq6ZGVWSFi1apOPHj3fpg8+fP6/hw4crNDRUkhQaGqq4uDidP3++S+sDAHSf36UQFxenQ4cOtVlWVVWluLi4gIcCADjD72MKy5Yt0+OPP65p06ZpxIgRqq2t1dtvv61169Z16YPj4+NVV1cnr9er0NBQeb1eXbx48Qu7mQAA9vF7pFBTU6Pdu3ebOY/GjRunXbt26cyZM1364GHDhikhIUGVlZWSpMrKSiUkJCgmJqZL6wMAdJ/fI4XS0lL98Ic/1OOPP95meVZWlnJzczt87+rVq7V//37V19crNzdXUVFRevPNN7Vy5UotX75cmzZtUmRkpEpKSrr2LQAAAWHLNBcrVqy47ZXPY8eO1euvv96ZvACAHtStaS7uuusuprkAgD6EaS4AAEanprkAAPRtfpcCAKDvoxQAAAalAAAwKAUAgEEpAAAMSgEAYFAKAACDUgAAGJQCAMCgFAAABqUAADAoBQCAQSkAAAxKAQBgUAoAAINSAAAYlAIAwKAUAAAGpQAAMCgFAIBBKQAADEoBAGBQCgAAg1IAABiUAgDAoBQAAAalAAAwKAUAgEEpAAAMSgEAYFAKAACDUgAAGJQCAMAIczqAJKWmpsrtdsvj8UiS8vLyNHXqVIdTAUD/ExSlIEkbN27U+PHjnY4BAP0au48AAEbQjBTy8vJkWZYmTpyoZcuWKTIy0ulIANDvBMVIYfv27SovL9fOnTtlWZaKi4udjgQA/VJQlEJ8fLwkye12Kzs7W0eOHHE4EQD0T46Xws2bN3X9+nVJkmVZ2rNnjxISEhxOBQD9k+PHFC5duqQnnnhCXq9XPp9PY8eOVVFRkdOxAKBfcrwURo4cqTfeeMPpGAAABcHuIwBA8KAUAAAGpQAAMCgFAIBBKQAADEoBAGBQCgAAg1IAABiUAgDAoBQAAAalAAAwKAUAgEEpAAAMSgEAYFAKAACDUgAAGJQCAMCgFAAABqUAADAoBQCAQSkAAAxKAQBgUAoAAINSAAAYlAIAwKAUAAAGpQAAMCgFAIBBKQAADEoBAGBQCgAAg1IAABiUAgDAoBQAAAalAAAwgqIUampqlJWVpbS0NGVlZen06dNORwKAfikoSqGoqEjZ2dnat2+fsrOzVVhY6HQkAOiXwpwOcOnSJR07dkxbt26VJKWnp+vZZ5/V5cuXFRMT49c6QkJcHT5/V/TgbufsK+60rfzhjhwWgCR9Q3e3510R/v2N9weB+NsceBd/m5/raHt29JzLsiyrJwL56+jRo/r5z3+uN9980yybPXu21q1bp/vvv9/BZADQ/wTF7iMAQHBwvBTi4+NVV1cnr9crSfJ6vbp48aLi4+MdTgYA/Y/jpTBs2DAlJCSosrJSklRZWamEhAS/jycAAALH8WMKknTq1CktX75c165dU2RkpEpKSjRmzBinYwFAvxMUpQAACA6O7z4CAAQPSgEAYFAKAACDUgAAGI5Pc9Ebfec731Fzc7NaWlp0+vRpjRs3TpJ0/fp1RUVFadeuXQ4n7DtSU1Pldrvl8XgkSSkpKXrmmWfavKagoECZmZlKTk52ImKvsHfvXr344ouyLEtNTU26//779ctf/rLd1589e1Z/+ctflJWVZWPK4NfZ7dgrWeiyM2fOWJMmTTK/v/vuu1ZmZma319va2trtdfQV06dPt06cONHu82yrO6urq7NSUlKs2tpay7Isy+fzWf/4xz86fE+g/pb7kq5sx96I3UcB5vV6VVhYqDlz5mju3Lk6deqUJGnXrl168sknzetu/X3Xrl165JFHtHTpUqWnp+vkyZOOZO8NbretfvCDH+jAgQNORwta9fX1CgsLU1RUlCTJ5XLpK1/5iiTppz/9qebPn685c+Zo6dKlunr1qiSpuLhYp06dUkZGRpu/2/6sve149uxZpaSkmNfd+vvnP2/YsEHz5s1TWlqaqqqqHMnvL3YfBdgHH3ygNWvWqLi4WJs3b9amTZv8Gl6+9957Kisr05e//GUbUvYuTz75pNl99L3vfY9t1Un33XefJkyYoGnTpiklJUVJSUnKyMhQdHS0CgoKzOwBGzZs0Msvv6y8vDwVFhaqpKSEXaG3aG873klDQ4MSExP1k5/8ROXl5Vq/fr127NhhQ+KuYaQQYKNHjzb/F5aYmKgzZ8749b6kpCT+kWvHxo0bVVZWprKyMrndbrZVJ4WEhGjTpk165ZVXlJKSooMHD2ru3LlqaGhQWVmZGSlUVlbq/fffdzpu0GpvO34+umrPoEGDNH36dEmd+zfBKYwUAsztdpufQ0JC1NraKkkKDQ2Vz+czzzU1NbV53+DB3PPBX2yrrhk/frzGjx+vnJwczZ49W7/73e9UXl6uHTt2KCYmRhUVFXrttdecjhn0/nM7VldXy7plYoj//G+7vX8TghUjBZvcc889OnHihJqbm9Xc3Kx9+/Y5HQn9RF1dnf7617+a3y9cuKDLly/L5XIpIiJCUVFRam5u1s6dO81rIiIi9MknnzgRN2i1tx3HjBmjlpYWffTRR5JkJvfsrRgp2CQxMVFTpkzRww8/rLi4ON133336+OOPnY6FfqC1tVUvvPCCzp07pwEDBsjn8+npp5/Wt7/9bVVXVystLU3R0dFKTk7W3//+d0nSvffeq9GjRys9PV1jxozRxo0bHf4WzmtvO06YMEEFBQXKzc1VTEyMpk2b5nTUbmFCPACAwe4jAIBBKQAADEoBAGBQCgAAg1IAABiUAhAAy5cv14YNG5yOAXQbpQAAMCgFAIBBKQBdcOzYMWVmZurrX/+6nn76aTPfzdWrV7V48WJNnjxZDz74oBYvXqwLFy5I+uwGLfPnz2+znq1bt2rJkiW25wfaQykAndTc3KylS5cqIyNDhw4d0syZM7V//35Jks/n0/z583XgwAEdOHBAHo9HxcXFkqQZM2bo7Nmz5h4bklRWVqZ58+Y58j2A26EUgE5677331NLSokWLFik8PFwzZ87UAw88IEmKjo5WWlqaBg4cqIiICC1ZskSHDx+W9NlsmbNmzVJ5ebkkqbq6WufOnTPTKgPBgFIAOunixYsaPny4XC6XWTZixAhJ0qeffqrCwkJNnz5dSUlJysnJ0bVr1+T1eiVJmZmZqqiokGVZKisr06xZs9pMrQw4jVIAOik2NlZ1dXVt5tCvra2VJP32t79VTU2NXnvtNR05ckTbt2+XJPPaxMREhYeHq6qqSpWVlZo7d679XwDoAKUAdFJiYqLCwsK0bds2tbS0aP/+/WbK6Rs3bsjj8SgyMlINDQ369a9//YX3z5s3T8XFxQoLC1NycrLd8YEOUQpAJ7ndbr3wwgvavXu3Jk2apD179uib3/ymJGnRokVqamrS5MmTlZWVpalTp37h/RkZGaqurmaUgKDE/RQAmzU2NmrKlCnavXu3Ro0a5XQcoA1GCoDNXn31VT3wwAMUAoISt+MEbJSamirLslRaWup0FOC22H0EADDYfQQAMCgFAIBBKQAADEoBAGBQCgAAg1IAABj/D4HlnQiaHAV7AAAAAElFTkSuQmCC
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-python"><pre><span></span><span class="c1"># Line plot</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>

<span class="c1"># Load the flights dataset</span>
<span class="n">flights</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">load_dataset</span><span class="p">(</span><span class="s2">&quot;flights&quot;</span><span class="p">)</span>

<span class="c1"># Plot the number of passengers over time</span>
<span class="n">sns</span><span class="o">.</span><span class="n">lineplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s2">&quot;year&quot;</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="s2">&quot;passengers&quot;</span><span class="p">,</span> <span class="n">data</span><span class="o">=</span><span class="n">flights</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[&nbsp;]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.axes._subplots.AxesSubplot at 0x7fb349cf86d0&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-python"><pre><span></span><span class="c1"># Scatter plot</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>

<span class="c1"># Load the iris dataset</span>
<span class="n">iris</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">load_dataset</span><span class="p">(</span><span class="s2">&quot;iris&quot;</span><span class="p">)</span>

<span class="c1"># Plot sepal length vs sepal width</span>
<span class="n">sns</span><span class="o">.</span><span class="n">scatterplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s2">&quot;sepal_length&quot;</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="s2">&quot;sepal_width&quot;</span><span class="p">,</span> <span class="n">data</span><span class="o">=</span><span class="n">iris</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[&nbsp;]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.axes._subplots.AxesSubplot at 0x7fb349cd3280&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-python"><pre><span></span><span class="c1"># Box plot</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>

<span class="c1"># Load the tips dataset</span>
<span class="n">tips</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">load_dataset</span><span class="p">(</span><span class="s2">&quot;tips&quot;</span><span class="p">)</span>

<span class="c1"># Plot the total bill amount for each day</span>
<span class="n">sns</span><span class="o">.</span><span class="n">boxplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s2">&quot;day&quot;</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="s2">&quot;total_bill&quot;</span><span class="p">,</span> <span class="n">data</span><span class="o">=</span><span class="n">tips</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[&nbsp;]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.axes._subplots.AxesSubplot at 0x7fb349c837f0&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-python"><pre><span></span><span class="c1"># Heatmap</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>

<span class="c1"># Load the flights dataset</span>
<span class="n">flights</span> <span class="o">=</span> <span class="n">sns</span><span class="o">.</span><span class="n">load_dataset</span><span class="p">(</span><span class="s2">&quot;flights&quot;</span><span class="p">)</span>

<span class="c1"># Create a pivot table showing the average number of passengers for each month and year</span>
<span class="n">pivot</span> <span class="o">=</span> <span class="n">flights</span><span class="o">.</span><span class="n">pivot_table</span><span class="p">(</span><span class="n">index</span><span class="o">=</span><span class="s2">&quot;month&quot;</span><span class="p">,</span> <span class="n">columns</span><span class="o">=</span><span class="s2">&quot;year&quot;</span><span class="p">,</span> <span class="n">values</span><span class="o">=</span><span class="s2">&quot;passengers&quot;</span><span class="p">)</span>

<span class="c1"># Draw a heatmap with the pivot table values</span>
<span class="n">sns</span><span class="o">.</span><span class="n">heatmap</span><span class="p">(</span><span class="n">pivot</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[&nbsp;]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.axes._subplots.AxesSubplot at 0x7fb349c27e80&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
    </div>
  </div>
</body>

 


</html>
