---
title: Font class
second_title: Aspose.Words for Python via .NET API Reference
description: "Contains font attributes (font name, font size, color, and so on) for an object"
type: docs
weight: 410
url: /python-net/aspose.words/font/
---

## Font class

Contains font attributes (font name, font size, color, and so on) for an object.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/net/working-with-fonts/) documentation article.




You do not create instances of the [Font](./) class directly. You just use
[Font](./) to access the font properties of the various objects such as [Run](../run/),
[Paragraph](../paragraph/), [Style](../style/), [DocumentBuilder](../documentbuilder/).




### Properties

| Name | Description |
| --- | --- |
| [all_caps](./all_caps/) | True if the font is formatted as all capital letters. |
| [auto_color](./auto_color/) | Returns the present calculated color of the text (black or white) to be used for 'auto color'. If the color is not 'auto' then returns [Font.color](./color/). |
| [bidi](./bidi/) | Specifies whether the contents of this run shall have right-to-left characteristics. |
| [bold](./bold/) | True if the font is formatted as bold. |
| [bold_bi](./bold_bi/) | True if the right-to-left text is formatted as bold. |
| [border](./border/) | Returns a [Border](../border/) object that specifies border for the font. |
| [color](./color/) | Gets or sets the color of the font. |
| [complex_script](./complex_script/) | Specifies whether the contents of this run shall be treated as complex script text regardless of their Unicode character values when determining the formatting for this run. |
| [double_strike_through](./double_strike_through/) | True if the font is formatted as double strikethrough text. |
| [emboss](./emboss/) | True if the font is formatted as embossed. |
| [emphasis_mark](./emphasis_mark/) | Gets or sets the emphasis mark applied to this formatting. |
| [engrave](./engrave/) | True if the font is formatted as engraved. |
| [fill](./fill/) | Gets fill formatting for the [Font](./). |
| [hidden](./hidden/) | True if the font is formatted as hidden text. |
| [highlight_color](./highlight_color/) | Gets or sets the highlight (marker) color. |
| [italic](./italic/) | True if the font is formatted as italic. |
| [italic_bi](./italic_bi/) | True if the right-to-left text is formatted as italic. |
| [kerning](./kerning/) | Gets or sets the font size at which kerning starts. |
| [line_spacing](./line_spacing/) | Returns line spacing of this font (in points). |
| [locale_id](./locale_id/) | Gets or sets the locale identifier (language) of the formatted characters. |
| [locale_id_bi](./locale_id_bi/) | Gets or sets the locale identifier (language) of the formatted right-to-left characters. |
| [locale_id_far_east](./locale_id_far_east/) | Gets or sets the locale identifier (language) of the formatted Asian characters. |
| [name](./name/) | Gets or sets the name of the font. |
| [name_ascii](./name_ascii/) | Returns or sets the font used for Latin text (characters with character codes from 0 (zero) through 127). |
| [name_bi](./name_bi/) | Returns or sets the name of the font in a right-to-left language document. |
| [name_far_east](./name_far_east/) | Returns or sets an East Asian font name. |
| [name_other](./name_other/) | Returns or sets the font used for characters with character codes from 128 through 255. |
| [no_proofing](./no_proofing/) | True when the formatted characters are not to be spell checked. |
| [outline](./outline/) | True if the font is formatted as outline. |
| [position](./position/) | Gets or sets the position of text (in points) relative to the base line. A positive number raises the text, and a negative number lowers it. |
| [scaling](./scaling/) | Gets or sets character width scaling in percent. |
| [shading](./shading/) | Returns a [Shading](../shading/) object that refers to the shading formatting for the font. |
| [shadow](./shadow/) | True if the font is formatted as shadowed. |
| [size](./size/) | Gets or sets the font size in points. |
| [size_bi](./size_bi/) | Gets or sets the font size in points used in a right-to-left document. |
| [small_caps](./small_caps/) | True if the font is formatted as small capital letters. |
| [snap_to_grid](./snap_to_grid/) | Specifies whether the current font should use the document grid characters per line settings when laying out. |
| [spacing](./spacing/) | Returns or sets the spacing (in points) between characters . |
| [strike_through](./strike_through/) | True if the font is formatted as strikethrough text. |
| [style](./style/) | Gets or sets the character style applied to this formatting. |
| [style_identifier](./style_identifier/) | Gets or sets the locale independent style identifier of the character style applied to this formatting. |
| [style_name](./style_name/) | Gets or sets the name of the character style applied to this formatting. |
| [subscript](./subscript/) | True if the font is formatted as subscript. |
| [superscript](./superscript/) | True if the font is formatted as superscript. |
| [text_effect](./text_effect/) | Gets or sets the font animation effect. |
| [theme_color](./theme_color/) | Gets or sets the theme color in the applied color scheme that is associated with this [Font](./) object. |
| [theme_font](./theme_font/) | Gets or sets the theme font in the applied font scheme that is associated with this [Font](./) object. |
| [theme_font_ascii](./theme_font_ascii/) | Gets or sets the theme font used for Latin text (characters with character codes from 0 (zero) through 127) in the applied font scheme that is associated with this [Font](./) object. |
| [theme_font_bi](./theme_font_bi/) | Gets or sets the theme font in the applied font scheme that is associated with this [Font](./) object in a right-to-left language document. |
| [theme_font_far_east](./theme_font_far_east/) | Gets or sets the East Asian theme font in the applied font scheme that is associated with this [Font](./) object. |
| [theme_font_other](./theme_font_other/) | Gets or sets the theme font used for characters with character codes from 128 through 255 in the applied font scheme that is associated with this [Font](./) object. |
| [tint_and_shade](./tint_and_shade/) | Gets or sets a double value that lightens or darkens a color. |
| [underline](./underline/) | Gets or sets the type of underline applied to the font. |
| [underline_color](./underline_color/) | Gets or sets the color of the underline applied to the font. |

### Methods

| Name | Description |
| --- | --- |
|[ clear_formatting()](./clear_formatting/#default) | Resets to default font formatting. |
|[ has_dml_effect(dml_effect_type)](./has_dml_effect/#textdmleffect) | Checks if particular DrawingML text effect is applied. |

### Examples

Shows how to insert a string surrounded by a border into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.border.color = drawing.Color.green
builder.font.border.line_width = 2.5
builder.font.border.line_style = aw.LineStyle.DASH_DOT_STROKER

builder.write("Text surrounded by green border.")

doc.save(ARTIFACTS_DIR + "Border.font_border.docx")
```

Shows how to format a run of text using its font property.

```python
doc = aw.Document()
run = aw.Run(doc, "Hello world!")

font = run.font
font.name = "Courier New"
font.size = 36
font.highlight_color = drawing.Color.yellow

doc.first_section.body.first_paragraph.append_child(run)
doc.save(ARTIFACTS_DIR + "Font.create_formatted_run.docx")
```

Shows how to create and use a paragraph style with list formatting.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Create a custom paragraph style.
style = doc.styles.add(aw.StyleType.PARAGRAPH, "MyStyle1")
style.font.size = 24
style.font.name = "Verdana"
style.paragraph_format.space_after = 12

# Create a list and make sure the paragraphs that use this style will use this list.
style.list_format.list = doc.lists.add(aw.lists.ListTemplate.BULLET_DEFAULT)
style.list_format.list_level_number = 0

# Apply the paragraph style to the document builder's current paragraph, and then add some text.
builder.paragraph_format.style = style
builder.writeln("Hello World: MyStyle1, bulleted list.")

# Change the document builder's style to one that has no list formatting and write another paragraph.
builder.paragraph_format.style = doc.styles.get_by_name("Normal")
builder.writeln("Hello World: Normal.")

builder.document.save(ARTIFACTS_DIR + "Styles.paragraph_style_bulleted_list.docx")
```

### See Also

* module [aspose.words](../)

