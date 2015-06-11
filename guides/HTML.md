## HTML - Table of Contents

 1. [HTTP content type](#html-content-type)
 2. [Doctype](#doctype)
 3. [Language](#language)
 4. [Encoding](#encoding)
 5. [Elements and Attributes](#elements-and-attributes)
 6. [Indentation](#indentation)
 7. [Validation](#validation)

<a name="html-content-type"></a>
### HTTP content type

You MUST use the `text/html` content type with a UTF-8 encoding:

```
Content-Type: text/html; charset=utf-8
```

<a name="doctype"></a>
### Doctype

You MUST use the minimal, versionless doctype.

```html
<!DOCTYPE html>
```

<a name="language"></a>
### Language

You MUST define which language the page is written in.

```html
<html lang="de">
```

<a name="encoding"></a>
### Encoding

You MUST define the character encoding using the minimal charset `META`
element. The encoding SHOULD be defined as early as possible.

```html
<meta charset="utf-8">
```

<a name="elements-and-attributes"></a>
### Elements and attributes

All element and attribute names SHOULD be lowercase. Attribute values
SHOULD be double-quoted. Optional closing tags SHOULD be included.
Self-closing elements SHOULD NOT be closed. Optional attributes SHOULD
be omitted. Always include `HTML`, `HEAD` and `BODY` tags.

 * No `type` or `language` attributes on `SCRIPT` elements.
 * No `type` attribute on `LINK` or `STYLE` elements.

```html
<script src="..."></script>
<script></script>
<link rel="stylesheet" href="...">
<style></style>
```

<a name="indentation"></a>
### Indentation

You MUST NOT indent inside `HTML`, `BODY`, `SCRIPT`, or `STYLE`. Indent
inside `HEAD` and all other block elements.

List items and all table elements (like `CAPTION`, `THEAD`, `TFOOT`,
`TBODY`, `TR`, `TH`, and `TD`) SHOULD stay on their own line and be
indented, too.

<a name="semantics"></a>
### Layered semantic markup / principles

 * Use semantic class/ID names and appropriate HTML elements for
   content as defined in
   [The Elements of HTML](http://developers.whatwg.org/semantics.html#semantics).
 * Actual `P` elements MUST be used for paragraph delimiters as opposed
   to multiple `BR` elements.
 * `DL` (definition lists) and `BLOCKQUOTE` SHOULD be used when
   appropriate.
 * Items in list form SHOULD always be housed in a `UL`, `OL`, or `DL`,
   never a set of `DIV` or `P` elements.
 * Inline CSS or inline JavaScript MUST NOT be used.
 * Dashes (not underscores) MUST be used as word delimiters in class/ID
   names.
 * Tables SHOULD NOT be used for page layout.
 * `THEAD`, `TBODY`, and `TH` elements (and `scope` attribute) SHOULD be
   used when appropriate.
 * Use `LABEL` elements to label each form field, the `for` attribute
   SHOULD associate itself with the form field, so users can click the
   labels. `cursor: pointer;` on the label is wise, as well.
 * [Microformats](http://microformats.org/) and Microdata SHOULD be used
   where appropriate, specifically
   [hCard](http://microformats.org/wiki/hcard) and
   [adr](http://microformats.org/wiki/adr).
 * Always use the appropriate case for headers and titles. Do not use
   all caps or all lowercase titles in markup, instead apply the CSS
   property `text-transform`.

<a name="validation"></a>
### Validation

All HTML documents SHOULD be verified against the
[W3C validator](http://validator.w3.org/nu/) to ensure that the markup
is well formed. This in and of itself is not directly indicative of good
code, but it helps to weed out problems that are able to be tested via
automation. It is no substitute for manual code review.

