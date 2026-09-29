---
title: HtmlSaveOptions.font_resources_subsetting_size_threshold property
linktitle: font_resources_subsetting_size_threshold property
articleTitle: font_resources_subsetting_size_threshold property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.font_resources_subsetting_size_threshold property. Controls which font resources need subsetting when saving to HTML, MHTML or EPUB"
type: docs
weight: 290
url: /it/python-net/aspose.words.saving/htmlsaveoptions/font_resources_subsetting_size_threshold/
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
# Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions per configurare il sottoinsieme dei font.
# Supponiamo di impostare il flag "export_font_resources" su "True" e di specificare anche una cartella nella proprietà "fonts_folder".
# In tal caso, l'operazione di salvataggio creerà quella cartella e vi inserirà un file .ttf all'interno
# in quella cartella per ogni font utilizzato dal nostro documento.
# Ogni file .ttf conterrà l'intero set di glifi di quel font,
# il che potrebbe potenzialmente generare un file molto grande che accompagna il documento.
# Quando applichiamo il subset a un font, i suoi dati grezzi esportati conterranno solo i glifi che il documento è
# utilizza invece l'intero set di glifi. Se il testo nel nostro documento utilizza solo una piccola frazione del set di glifi di un font
# set di glifi, allora il subset ridurrà significativamente le dimensioni dei nostri documenti di output.
# Possiamo usare la proprietà "font_resources_subsetting_size_threshold" per definire una dimensione di file .ttf, in byte.
# Se un font esportato genera un file di dimensione maggiore di quella, allora l'operazione di salvataggio applicherà il subset a quel font.
# Impostare una soglia di 0 applica il subset a tutti i font,
# e impostandola a "2**31 - 1" disabilita effettivamente il subset.
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
    # Per impostazione predefinita, i file .ttf per ciascuno dei nostri tre font supereranno i 700 MB.
    # Il subset li ridurrà tutti a meno di 30 MB.
    font_file_size = os.path.getsize(filename)
    self.assertTrue(font_file_size > 700000 or font_file_size < 30000)
    self.assertTrue(max(font_resources_subsetting_size_threshold, 30000) > font_file_size)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.export_font_resources](../export_font_resources/)

