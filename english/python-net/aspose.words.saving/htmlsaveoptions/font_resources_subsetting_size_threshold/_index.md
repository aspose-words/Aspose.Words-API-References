---
title: font_resources_subsetting_size_threshold property
second_title: Aspose.Words for Python via .NET API Reference
description: "Controls which font resources need subsetting when saving to HTML, MHTML or EPUB"
type: docs
weight: 310
url: /python-net/aspose.words.saving/htmlsaveoptions/font_resources_subsetting_size_threshold/
---

## HtmlSaveOptions.font_resources_subsetting_size_threshold property

Controls which font resources need subsetting when saving to HTML, MHTML or EPUB.
Default is ``0``.


[HtmlSaveOptions.export_font_resources](../export_font_resources/) allows exporting fonts as subsidiary files or as parts of the output
package. If the document uses many fonts, especially with large number of glyphs, then output size can grow
significantly. Font subsetting reduces the size of the exported font resource by filtering out glyphs that
are not used by the current document.

Font subsetting works as follows:


* By default, all exported fonts are subsetted.
  
* Setting [HtmlSaveOptions.font_resources_subsetting_size_threshold](./) to a positive value 
  instructs Aspose.Words to subset fonts which file size is larger than the specified value.
  
* Setting the property to System.Int32.MaxValue
  suppresses font subsetting.
  
**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable
font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not
allow web downloading of their fonts in any form. License agreements that cover some fonts specifically note that usage via **@font-face** rules
in CSS style sheets is not allowed. Font subsetting can also violate license terms.





### Examples

Shows how to work with font subsetting.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.name = "Arial"
builder.writeln("Hello world!")
builder.font.name = "Times New Roman"
builder.writeln("Hello world!")
builder.font.name = "Courier New"
builder.writeln("Hello world!")

# When we save the document to HTML, we can pass a SaveOptions object configure font subsetting.
# Suppose we set the "export_font_resources" flag to "True" and also name a folder in the "fonts_folder" property.
# In that case, the saving operation will create that folder and place a .ttf file inside
# that folder for each font that our document uses.
# Each .ttf file will contain that font's entire glyph set,
# which may potentially result in a very large file that accompanies the document.
# When we apply subsetting to a font, its exported raw data will only contain the glyphs that the document is
# using instead of the entire glyph set. If the text in our document only uses a small fraction of a font's
# glyph set, then subsetting will significantly reduce our output documents' size.
# We can use the "font_resources_subsetting_size_threshold" property to define a .ttf file size, in bytes.
# If an exported font creates a size bigger file than that, then the save operation will apply subsetting to that font.
# Setting a threshold of 0 applies subsetting to all fonts,
# and setting it to "2**31 - 1" effectively disables subsetting.
fonts_folder = ARTIFACTS_DIR + "HtmlSaveOptions.font_subsetting.fonts"

if os.path.exists(fonts_folder):
    shutil.rmtree(fonts_folder)

options = aw.saving.HtmlSaveOptions()
options.export_font_resources = True
options.fonts_folder = fonts_folder
options.font_resources_subsetting_size_threshold = font_resources_subsetting_size_threshold

doc.save(ARTIFACTS_DIR + "HtmlSaveOptions.font_subsetting.html", options)

font_file_names = glob.glob(fonts_folder + "/*.ttf")

self.assertEqual(3, len(font_file_names))

for filename in font_file_names:
    # By default, the .ttf files for each of our three fonts will be over 700MB.
    # Subsetting will reduce them all to under 30MB.
    font_file_size = os.path.getsize(filename)

    self.assertTrue(font_file_size > 700000 or font_file_size < 30000)
    self.assertTrue(max(font_resources_subsetting_size_threshold, 30000) > font_file_size)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.export_font_resources](../export_font_resources/)

