---
title: HtmlSaveOptions.font_resources_subsetting_size_threshold property
linktitle: font_resources_subsetting_size_threshold property
articleTitle: font_resources_subsetting_size_threshold property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.font_resources_subsetting_size_threshold property. Controls which font resources need subsetting when saving to HTML, MHTML or EPUB"
type: docs
weight: 290
url: /de/python-net/aspose.words.saving/htmlsaveoptions/font_resources_subsetting_size_threshold/
---

## HtmlSaveOptions.font_resources_subsetting_size_threshold property

Controls which font resources need subsetting when saving to HTML, MHTML or EPUB.
Default is ``0``.



```python
@property
def font_resources_subsetting_size_threshold(self) -> int:
    ...

@font_resources_subsetting_size_threshold.setter
def font_resources_subsetting_size_threshold(self, value: int):
    ...

```

### Remarks

[HtmlSaveOptions.export_font_resources](../export_font_resources/) allows exporting fonts as subsidiary files or as parts of the output
package. If the document uses many fonts, especially with large number of glyphs, then output size can grow
significantly. Font subsetting reduces the size of the exported font resource by filtering out glyphs that
are not used by the current document.

Font subsetting works as follows:


* By default, all exported fonts are subsetted.
  
* Setting [HtmlSaveOptions.font_resources_subsetting_size_threshold](./) to a positive value
  instructs Aspose.Words to subset fonts which file size is larger than the specified value.
  
* Setting the property to int.MaxValue C# constant
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
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Times New Roman'
builder.writeln('Hello world!')
builder.font.name = 'Courier New'
builder.writeln('Hello world!')
# Wenn wir das Dokument nach HTML speichern, können wir ein SaveOptions‑Objekt übergeben, um die Schriftart‑Subset‑Erstellung zu konfigurieren.
# Angenommen, wir setzen das Flag "export_font_resources" auf "True" und geben außerdem einen Ordner in der Eigenschaft "fonts_folder" an.
# In diesem Fall wird der Speicher‑Vorgang diesen Ordner erstellen und eine .ttf‑Datei darin ablegen
# diesen Ordner für jede Schriftart, die unser Dokument verwendet.
# Jede .ttf‑Datei wird den gesamten Glyphensatz dieser Schriftart enthalten,
# was potenziell zu einer sehr großen Datei führen kann, die das Dokument begleitet.
# Wenn wir ein Subsetting auf eine Schriftart anwenden, enthalten die exportierten Rohdaten nur die Glyphen, die das Dokument ist
# statt des gesamten Glyphensatzes verwendet. Wenn der Text in unserem Dokument nur einen kleinen Bruchteil eines Schriftsatzes verwendet
# Glyphensatz, dann wird das Subsetting die Größe unserer Ausgabedokumente erheblich reduzieren.
# Wir können die Eigenschaft "font_resources_subsetting_size_threshold" verwenden, um eine .ttf-Dateigröße in Bytes zu definieren.
# Wenn eine exportierte Schriftart eine größere Datei als diese erzeugt, wird der Speichervorgang Subsetting auf diese Schriftart anwenden.
# Das Festlegen eines Schwellenwerts von 0 wendet Subsetting auf alle Schriftarten an,
# und das Festlegen auf "2**31 - 1" deaktiviert Subsetting effektiv.
fonts_folder = ARTIFACTS_DIR + 'HtmlSaveOptions.font_subsetting.fonts'
if os.path.exists(fonts_folder):
    shutil.rmtree(fonts_folder)
options = aw.saving.HtmlSaveOptions()
options.export_font_resources = True
options.fonts_folder = fonts_folder
options.font_resources_subsetting_size_threshold = font_resources_subsetting_size_threshold
doc.save(ARTIFACTS_DIR + 'HtmlSaveOptions.font_subsetting.html', options)
font_file_names = glob.glob(fonts_folder + '/*.ttf')
self.assertEqual(3, len(font_file_names))
for filename in font_file_names:
    # Standardmäßig werden die .ttf-Dateien für jede unserer drei Schriftarten über 700 MB groß sein.
    # Subsetting wird sie alle auf unter 30 MB reduzieren.
    font_file_size = os.path.getsize(filename)
    self.assertTrue(font_file_size > 700000 or font_file_size < 30000)
    self.assertTrue(max(font_resources_subsetting_size_threshold, 30000) > font_file_size)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.export_font_resources](../export_font_resources/)

