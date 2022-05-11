---
title: Font
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 2600
url: /net/aspose.words/font/
---
## Font class

Contains font attributes (font name, font size, color, and so on) for an object.

```csharp
public class Font
```

## Properties

| Name | Description |
| --- | --- |
| [AllCaps](allcaps) { get; set; } | True if the font is formatted as all capital letters. |
| [AutoColor](autocolor) { get; } | Returns the present calculated color of the text (black or white) to be used for 'auto color'. If the color is not 'auto' then returns [`Color`](./color). |
| [Bidi](bidi) { get; set; } | Specifies whether the contents of this run shall have right-to-left characteristics. |
| [Bold](bold) { get; set; } | True if the font is formatted as bold. |
| [BoldBi](boldbi) { get; set; } | True if the right-to-left text is formatted as bold. |
| [Border](border) { get; } | Returns a Border object that specifies border for the font. |
| [Color](color) { get; set; } | Gets or sets the color of the font. |
| [ComplexScript](complexscript) { get; set; } | Specifies whether the contents of this run shall be treated as complex script text regardless of their Unicode character values when determining the formatting for this run. |
| [DoubleStrikeThrough](doublestrikethrough) { get; set; } | True if the font is formatted as double strikethrough text. |
| [Emboss](emboss) { get; set; } | True if the font is formatted as embossed. |
| [EmphasisMark](emphasismark) { get; set; } | Gets or sets the emphasis mark applied to this formatting. |
| [Engrave](engrave) { get; set; } | True if the font is formatted as engraved. |
| [Fill](fill) { get; } | Gets fill formatting for the Font. |
| [Hidden](hidden) { get; set; } | True if the font is formatted as hidden text. |
| [HighlightColor](highlightcolor) { get; set; } | Gets or sets the highlight (marker) color. |
| [Italic](italic) { get; set; } | True if the font is formatted as italic. |
| [ItalicBi](italicbi) { get; set; } | True if the right-to-left text is formatted as italic. |
| [Kerning](kerning) { get; set; } | Gets or sets the font size at which kerning starts. |
| [LineSpacing](linespacing) { get; } | Returns line spacing of this font (in points). |
| [LocaleId](localeid) { get; set; } | Gets or sets the locale identifier (language) of the formatted characters. |
| [LocaleIdBi](localeidbi) { get; set; } | Gets or sets the locale identifier (language) of the formatted right-to-left characters. |
| [LocaleIdFarEast](localeidfareast) { get; set; } | Gets or sets the locale identifier (language) of the formatted Asian characters. |
| [Name](name) { get; set; } | Gets or sets the name of the font. |
| [NameAscii](nameascii) { get; set; } | Returns or sets the font used for Latin text (characters with character codes from 0 (zero) through 127). |
| [NameBi](namebi) { get; set; } | Returns or sets the name of the font in a right-to-left language document. |
| [NameFarEast](namefareast) { get; set; } | Returns or sets an East Asian font name. |
| [NameOther](nameother) { get; set; } | Returns or sets the font used for characters with character codes from 128 through 255. |
| [NoProofing](noproofing) { get; set; } | True when the formatted characters are not to be spell checked. |
| [Outline](outline) { get; set; } | True if the font is formatted as outline. |
| [Position](position) { get; set; } | Gets or sets the position of text (in points) relative to the base line. A positive number raises the text, and a negative number lowers it. |
| [Scaling](scaling) { get; set; } | Gets or sets character width scaling in percent. |
| [Shading](shading) { get; } | Returns a Shading object that refers to the shading formatting for the font. |
| [Shadow](shadow) { get; set; } | True if the font is formatted as shadowed. |
| [Size](size) { get; set; } | Gets or sets the font size in points. |
| [SizeBi](sizebi) { get; set; } | Gets or sets the font size in points used in a right-to-left document. |
| [SmallCaps](smallcaps) { get; set; } | True if the font is formatted as small capital letters. |
| [SnapToGrid](snaptogrid) { get; set; } | Specifies whether the current font should use the document grid characters per line settings when laying out. |
| [Spacing](spacing) { get; set; } | Returns or sets the spacing (in points) between characters . |
| [StrikeThrough](strikethrough) { get; set; } | True if the font is formatted as strikethrough text. |
| [Style](style) { get; set; } | Gets or sets the character style applied to this formatting. |
| [StyleIdentifier](styleidentifier) { get; set; } | Gets or sets the locale independent style identifier of the character style applied to this formatting. |
| [StyleName](stylename) { get; set; } | Gets or sets the name of the character style applied to this formatting. |
| [Subscript](subscript) { get; set; } | True if the font is formatted as subscript. |
| [Superscript](superscript) { get; set; } | True if the font is formatted as superscript. |
| [TextEffect](texteffect) { get; set; } | Gets or sets the font animation effect. |
| [ThemeColor](themecolor) { get; set; } | Gets or sets the theme color in the applied color scheme that is associated with this Font object. |
| [ThemeFont](themefont) { get; set; } | Gets or sets the theme font in the applied font scheme that is associated with this Font object. |
| [ThemeFontAscii](themefontascii) { get; set; } | Gets or sets the theme font used for Latin text (characters with character codes from 0 (zero) through 127) in the applied font scheme that is associated with this Font object. |
| [ThemeFontBi](themefontbi) { get; set; } | Gets or sets the theme font in the applied font scheme that is associated with this Font object in a right-to-left language document. |
| [ThemeFontFarEast](themefontfareast) { get; set; } | Gets or sets the East Asian theme font in the applied font scheme that is associated with this Font object. |
| [ThemeFontOther](themefontother) { get; set; } | Gets or sets the theme font used for characters with character codes from 128 through 255 in the applied font scheme that is associated with this Font object. |
| [TintAndShade](tintandshade) { get; set; } | Gets or sets a double value that lightens or darkens a color. |
| [Underline](underline) { get; set; } | Gets or sets the type of underline applied to the font. |
| [UnderlineColor](underlinecolor) { get; set; } | Gets or sets the color of the underline applied to the font. |

## Methods

| Name | Description |
| --- | --- |
| [ClearFormatting](clearformatting)() | Resets to default font formatting. |
| [HasDmlEffect](hasdmleffect)(TextDmlEffect) | Checks if particular DrawingML text effect is applied. |

### Remarks

You do not create instances of the [`Font`](../font) class directly. You just use [`Font`](../font) to access the font properties of the various objects such as [`Run`](../run), [`Paragraph`](../paragraph), [`Style`](../style), [`DocumentBuilder`](../documentbuilder).

### Examples

Shows how to format a run of text using its font property.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

Shows how to insert a string surrounded by a border into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

Shows how to create and use a paragraph style with list formatting.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create a custom paragraph style.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Create a list and make sure the paragraphs that use this style will use this list.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Apply the paragraph style to the document builder's current paragraph, and then add some text.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Change the document builder's style to one that has no list formatting and write another paragraph.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### See Also

* namespace [Aspose.Words](../../aspose.words)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
