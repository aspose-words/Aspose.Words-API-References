---
title: HtmlSaveOptions.font_resources_subsetting_size_threshold property
linktitle: font_resources_subsetting_size_threshold property
articleTitle: font_resources_subsetting_size_threshold property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.font_resources_subsetting_size_threshold property. Controls which font resources need subsetting when saving to HTML, MHTML or EPUB"
type: docs
weight: 290
url: /fr/python-net/aspose.words.saving/htmlsaveoptions/font_resources_subsetting_size_threshold/
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
# Lorsque nous enregistrons le document en HTML, nous pouvons passer un objet SaveOptions pour configurer le sous-ensemble de polices.
# Supposons que nous définissions le drapeau "export_font_resources" sur "True" et que nous indiquions également un dossier dans la propriété "fonts_folder".
# Dans ce cas, l'opération d'enregistrement créera ce dossier et y placera un fichier .ttf
# dans ce dossier pour chaque police utilisée par notre document.
# Chaque fichier .ttf contiendra l'ensemble complet des glyphes de cette police,
# ce qui peut potentiellement entraîner un fichier très volumineux qui accompagne le document.
# Lorsque nous appliquons le sous-ensemble à une police, ses données brutes exportées ne contiendront que les glyphes que le document est
# utilise à la place de l'ensemble complet de glyphes. Si le texte de notre document n'utilise qu'une petite fraction du jeu de glyphes d'une police
# jeu de glyphes, alors le sous-ensemble réduira de façon significative la taille de nos documents de sortie.
# Nous pouvons utiliser la propriété "font_resources_subsetting_size_threshold" pour définir une taille de fichier .ttf, en octets.
# Si une police exportée crée un fichier de taille supérieure à cela, alors l'opération d'enregistrement appliquera le sous-ensemble à cette police.
# Définir un seuil de 0 applique le sous-ensemble à toutes les polices,
# et le définir à "2**31 - 1" désactive effectivement le sous-ensemble.
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
    # Par défaut, les fichiers .ttf pour chacune de nos trois polices dépasseront 700 Mo.
    # Le sous-ensemble les réduira tous à moins de 30 Mo.
    font_file_size = os.path.getsize(filename)
    self.assertTrue(font_file_size > 700000 or font_file_size < 30000)
    self.assertTrue(max(font_resources_subsetting_size_threshold, 30000) > font_file_size)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.export_font_resources](../export_font_resources/)

