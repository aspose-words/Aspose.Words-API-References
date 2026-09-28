---
title: HtmlSaveOptions.navigation_map_level property
linktitle: navigation_map_level property
articleTitle: navigation_map_level property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.navigation_map_level property. Specifies the maximum level of headings populated to the navigation map when exporting to EPUB, MOBI, or AZW3 formats"
type: docs
weight: 390
url: /de/python-net/aspose.words.saving/htmlsaveoptions/navigation_map_level/
---

## HtmlSaveOptions.navigation_map_level property

Specifies the maximum level of headings populated to the navigation map when exporting to EPUB, MOBI, or AZW3
formats. Default value is ``3``.



```python
@property
def navigation_map_level(self) -> int:
    ...

@navigation_map_level.setter
def navigation_map_level(self, value: int):
    ...

```

### Remarks

The navigation map allows user agents to provide an easy way of navigation through the document structure.
Usually navigation points correspond to headings in the document. In order to populate headings up to level **N**
assign this value to [HtmlSaveOptions.navigation_map_level](./).

By default, three levels of headings are populated: paragraphs of styles **Heading 1**, **Heading 2**
and **Heading 3**.
You can set this property to a value from 1 to 9 in order to request the corresponding maximum level.
Setting it to zero will reduce the navigation map to only the document root or roots of document parts.




### Examples

Shows how to generate table of contents for Azw3 documents.

```python
doc = aw.Document(file_name=MY_DIR + 'Big document.docx')
options = aw.saving.HtmlSaveOptions(aw.SaveFormat.AZW3)
options.navigation_map_level = 2
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.CreateAZW3Toc.azw3', save_options=options)
```

Shows how to generate table of contents for Mobi documents.

```python
doc = aw.Document(file_name=MY_DIR + 'Big document.docx')
options = aw.saving.HtmlSaveOptions(aw.SaveFormat.MOBI)
options.navigation_map_level = 5
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.CreateMobiToc.mobi', save_options=options)
```

Shows how to filter headings that appear in the navigation panel of a saved Epub document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Jeder Absatz, den wir mit einem "Heading"-Stil formatieren, kann als Überschrift dienen.
# Jede Überschrift kann zudem eine Ebene haben, die durch die Nummer ihres Überschriftsstils bestimmt wird.
# Die untenstehenden Überschriften haben die Ebenen 1‑3.
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 1')
builder.writeln('Heading #1')
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 2')
builder.writeln('Heading #2')
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 3')
builder.writeln('Heading #3')
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 1')
builder.writeln('Heading #4')
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 2')
builder.writeln('Heading #5')
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 3')
builder.writeln('Heading #6')
# Epub-Reader erstellen typischerweise ein Inhaltsverzeichnis für ihre Dokumente.
# Jeder Absatz mit einem "Heading"-Stil im Dokument erzeugt einen Eintrag in diesem Inhaltsverzeichnis.
# Wir können die Eigenschaft "NavigationMapLevel" verwenden, um eine maximale Überschriftenebene festzulegen.
# Der Epub-Reader wird keine Überschriften mit einer Ebene über der von uns angegebenen zum Inhaltsverzeichnis hinzufügen.
options = aw.saving.HtmlSaveOptions(aw.SaveFormat.EPUB)
options.navigation_map_level = 2
# Unser Dokument hat sechs Überschriften, von denen zwei über Ebene 2 liegen.
# Das Inhaltsverzeichnis für dieses Dokument wird vier Einträge haben.
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.EpubHeadings.epub', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

