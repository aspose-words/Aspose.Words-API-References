---
title: StructuredDocumentTag.contents_font property
linktitle: contents_font property
articleTitle: contents_font property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.contents_font property. Font formatting that will be applied to text entered into SDT."
type: docs
weight: 80
url: /de/python-net/aspose.words.markup/structureddocumenttag/contents_font/
---

## StructuredDocumentTag.contents_font property

Font formatting that will be applied to text entered into **SDT**.



```python
@property
def contents_font(self) -> aspose.words.Font:
    ...

```

### Examples

Shows how to create a structured document tag in a plain text box and modify its appearance.

```python
doc = aw.Document()
# Erstellen Sie ein strukturiertes Dokument-Tag, das Klartext enthält.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Legen Sie den Titel und die Farbe des Rahmens fest, der erscheint, wenn Sie mit der Maus über das strukturierte Dokument-Tag in Microsoft Word fahren.
tag.title = 'My plain text'
tag.color = aspose.pydrawing.Color.magenta
# Setzen Sie ein Tag für dieses strukturierte Dokument-Tag, das abrufbar ist
# als ein XML-Element mit dem Namen "tag", wobei die untenstehende Zeichenfolge im Attribut "@val" enthalten ist.
tag.tag = 'MyPlainTextSDT'
# Jedes strukturierte Dokument-Tag hat eine zufällige eindeutige ID.
self.assertTrue(tag.id > 0)
# Legen Sie die Schriftart für den Text innerhalb des strukturierten Dokument-Tags fest.
tag.contents_font.name = 'Arial'
# Legen Sie die Schriftart für den Text am Ende des strukturierten Dokument-Tags fest.
# Jeder Text, den wir im Dokumentkörper eingeben, nachdem wir das Tag mit den Pfeiltasten verlassen haben, verwendet diese Schriftart.
tag.end_character_font.name = 'Arial Black'
# Standardmäßig ist dies false und das Drücken von Enter innerhalb eines strukturierten Dokument-Tags bewirkt nichts.
# Wenn auf true gesetzt, kann unser strukturiertes Dokument-Tag mehrere Zeilen enthalten.
# Setzen Sie die Eigenschaft "Multiline" auf "false", um nur den Inhalt zu erlauben
# dieses strukturierten Dokument-Tags auf eine einzelne Zeile zu beschränken.
# Setzen Sie die Eigenschaft "Multiline" auf "true", um dem Tag zu erlauben, mehrere Zeilen Inhalt zu enthalten.
tag.multiline = True
# Setzen Sie die Eigenschaft "Appearance" auf "SdtAppearance.Tags", um Tags um den Inhalt anzuzeigen.
# Standardmäßig wird das strukturierte Dokument-Tag als BoundingBox angezeigt.
tag.appearance = aw.markup.SdtAppearance.TAGS
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(tag)
# Fügen Sie eine Kopie unseres strukturierten Dokument-Tags in einen neuen Absatz ein.
tag_clone = tag.clone(True).as_structured_document_tag()
builder.insert_paragraph()
builder.insert_node(tag_clone)
# Verwenden Sie die Methode "RemoveSelfOnly", um ein strukturiertes Dokument-Tag zu entfernen, während dessen Inhalt im Dokument erhalten bleibt.
tag_clone.remove_self_only()
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.PlainText.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

