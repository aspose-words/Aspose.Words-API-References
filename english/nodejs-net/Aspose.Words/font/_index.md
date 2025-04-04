---
title: Font class
linktitle: Font class
articleTitle: Font class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Font class. Contains font attributes (font name, font size, color, and so on) for an object"
type: docs
weight: 450
url: /nodejs-net/aspose.words/font/
---

## Font class

Contains font attributes (font name, font size, color, and so on) for an object.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/nodejs-net/working-with-fonts/) documentation article.




### Remarks

You do not create instances of the [Font](./) class directly. You just use
[Font](./) to access the font properties of the various objects such as [Run](../run/),
[Paragraph](../paragraph/), [Style](../style/), [DocumentBuilder](../documentbuilder/).




### Properties

| Name | Description |
| --- | --- |
| [allCaps](./allCaps/) | True if the font is formatted as all capital letters. |
| [autoColor](./autoColor/) | Returns the present calculated color of the text (black or white) to be used for 'auto color'. If the color is not 'auto' then returns [Font.color](./color/). |
| [bidi](./bidi/) | Specifies whether the contents of this run shall have right-to-left characteristics. |
| [bold](./bold/) | True if the font is formatted as bold. |
| [boldBi](./boldBi/) | True if the right-to-left text is formatted as bold. |
| [border](./border/) | Returns a [Border](../border/) object that specifies border for the font. |
| [color](./color/) | Gets or sets the color of the font. |
| [complexScript](./complexScript/) | Specifies whether the contents of this run shall be treated as complex script text regardless of their Unicode character values when determining the formatting for this run. |
| [doubleStrikeThrough](./doubleStrikeThrough/) | True if the font is formatted as double strikethrough text. |
| [emboss](./emboss/) | True if the font is formatted as embossed. |
| [emphasisMark](./emphasisMark/) | Gets or sets the emphasis mark applied to this formatting. |
| [engrave](./engrave/) | True if the font is formatted as engraved. |
| [fill](./fill/) | Gets fill formatting for the [Font](./). |
| [hidden](./hidden/) | True if the font is formatted as hidden text. |
| [highlightColor](./highlightColor/) | Gets or sets the highlight (marker) color. |
| [italic](./italic/) | True if the font is formatted as italic. |
| [italicBi](./italicBi/) | True if the right-to-left text is formatted as italic. |
| [kerning](./kerning/) | Gets or sets the font size at which kerning starts. |
| [lineSpacing](./lineSpacing/) | Returns line spacing of this font (in points). |
| [localeId](./localeId/) | Gets or sets the locale identifier (language) of the formatted characters. |
| [localeIdBi](./localeIdBi/) | Gets or sets the locale identifier (language) of the formatted right-to-left characters. |
| [localeIdFarEast](./localeIdFarEast/) | Gets or sets the locale identifier (language) of the formatted Asian characters. |
| [name](./name/) | Gets or sets the name of the font. |
| [nameAscii](./nameAscii/) | Returns or sets the font used for Latin text (characters with character codes from 0 (zero) through 127). |
| [nameBi](./nameBi/) | Returns or sets the name of the font in a right-to-left language document. |
| [nameFarEast](./nameFarEast/) | Returns or sets an East Asian font name. |
| [nameOther](./nameOther/) | Returns or sets the font used for characters with character codes from 128 through 255. |
| [noProofing](./noProofing/) | True when the formatted characters are not to be spell checked. |
| [numberSpacing](./numberSpacing/) | Gets or sets the spacing type of the numeral being displayed. |
| [outline](./outline/) | True if the font is formatted as outline. |
| [position](./position/) | Gets or sets the position of text (in points) relative to the base line. A positive number raises the text, and a negative number lowers it. |
| [scaling](./scaling/) | Gets or sets character width scaling in percent. |
| [shading](./shading/) | Returns a [Shading](../shading/) object that refers to the shading formatting for the font. |
| [shadow](./shadow/) | True if the font is formatted as shadowed. |
| [size](./size/) | Gets or sets the font size in points. |
| [sizeBi](./sizeBi/) | Gets or sets the font size in points used in a right-to-left document. |
| [smallCaps](./smallCaps/) | True if the font is formatted as small capital letters. |
| [snapToGrid](./snapToGrid/) | Specifies whether the current font should use the document grid characters per line settings when laying out. |
| [spacing](./spacing/) | Returns or sets the spacing (in points) between characters . |
| [strikeThrough](./strikeThrough/) | True if the font is formatted as strikethrough text. |
| [style](./style/) | Gets or sets the character style applied to this formatting. |
| [styleIdentifier](./styleIdentifier/) | Gets or sets the locale independent style identifier of the character style applied to this formatting. |
| [styleName](./styleName/) | Gets or sets the name of the character style applied to this formatting. |
| [subscript](./subscript/) | True if the font is formatted as subscript. |
| [superscript](./superscript/) | True if the font is formatted as superscript. |
| [textEffect](./textEffect/) | Gets or sets the font animation effect. |
| [themeColor](./themeColor/) | Gets or sets the theme color in the applied color scheme that is associated with this [Font](./) object. |
| [themeFont](./themeFont/) | Gets or sets the theme font in the applied font scheme that is associated with this [Font](./) object. |
| [themeFontAscii](./themeFontAscii/) | Gets or sets the theme font used for Latin text (characters with character codes from 0 (zero) through 127) in the applied font scheme that is associated with this [Font](./) object. |
| [themeFontBi](./themeFontBi/) | Gets or sets the theme font in the applied font scheme that is associated with this [Font](./) object in a right-to-left language document. |
| [themeFontFarEast](./themeFontFarEast/) | Gets or sets the East Asian theme font in the applied font scheme that is associated with this [Font](./) object. |
| [themeFontOther](./themeFontOther/) | Gets or sets the theme font used for characters with character codes from 128 through 255 in the applied font scheme that is associated with this [Font](./) object. |
| [tintAndShade](./tintAndShade/) | Gets or sets a double value that lightens or darkens a color. |
| [underline](./underline/) | Gets or sets the type of underline applied to the font. |
| [underlineColor](./underlineColor/) | Gets or sets the color of the underline applied to the font. |

### Methods

| Name | Description |
| --- | --- |
|[ clearFormatting()](./clearFormatting/#default) | Resets to default font formatting. |
|[ hasDmlEffect(dmlEffectType)](./hasDmlEffect/#textdmleffect) | Checks if particular DrawingML text effect is applied. |

### Examples

Shows how to create and use a paragraph style with list formatting.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Create a custom paragraph style.
let style = doc.styles.add(aw.StyleType.Paragraph, "MyStyle1");
style.font.size = 24;
style.font.name = "Verdana";
style.paragraphFormat.spaceAfter = 12;

// Create a list and make sure the paragraphs that use this style will use this list.
style.listFormat.list = doc.lists.add(aw.Lists.ListTemplate.BulletDefault);
style.listFormat.listLevelNumber = 0;

// Apply the paragraph style to the document builder's current paragraph, and then add some text.
builder.paragraphFormat.style = style;
builder.writeln("Hello World: MyStyle1, bulleted list.");

// Change the document builder's style to one that has no list formatting and write another paragraph.
builder.paragraphFormat.style = doc.styles.at("Normal");
builder.writeln("Hello World: Normal.");

builder.document.save(base.artifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

Shows how to format a run of text using its font property.

```js
let doc = new aw.Document();
let run = new aw.Run(doc, "Hello world!");

let font = run.font;
font.name = "Courier New";
font.size = 36;
font.highlightColor = "#FFFF00";

doc.firstSection.body.firstParagraph.appendChild(run);
doc.save(base.artifactsDir + "Font.CreateFormattedRun.docx");
```

Shows how to insert a string surrounded by a border into a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.font.border.color = "#008000";
builder.font.border.lineWidth = 2.5;
builder.font.border.lineStyle = aw.LineStyle.DashDotStroker;

builder.write("Text surrounded by green border.");

doc.save(base.artifactsDir + "Border.FontBorder.docx");
```

### See Also

* module [Aspose.Words](../)

