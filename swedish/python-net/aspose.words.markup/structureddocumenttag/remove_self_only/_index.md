---
title: StructuredDocumentTag.remove_self_only method
linktitle: remove_self_only method
articleTitle: remove_self_only method
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.remove_self_only method. Removes just this SDT node itself, but keeps the content of it inside the document tree."
type: docs
weight: 370
url: /sv/python-net/aspose.words.markup/structureddocumenttag/remove_self_only/
---

## remove_self_only() {#default}

Removes just this SDT node itself, but keeps the content of it inside the document tree.


```python
def remove_self_only(self):
    ...
```

### Examples

Shows how to create a structured document tag in a plain text box and modify its appearance.

```python
doc = aw.Document()
# Skapa en strukturerad dokumenttagg som kommer att innehålla vanlig text.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Ställ in titel och färg på ramen som visas när du för musen över den strukturerade dokumenttaggen i Microsoft Word.
tag.title = 'My plain text'
tag.color = aspose.pydrawing.Color.magenta
# Ställ in en tagg för detta strukturerade dokumenttagg, som är tillgänglig
# som ett XML-element med namnet "tag", med strängen nedan i dess "@val"-attribut.
tag.tag = 'MyPlainTextSDT'
# Varje strukturerat dokumenttagg har ett slumpmässigt unikt ID.
self.assertTrue(tag.id > 0)
# Ställ in teckensnittet för texten inne i det strukturerade dokumenttagget.
tag.contents_font.name = 'Arial'
# Ställ in teckensnittet för texten i slutet av det strukturerade dokumenttagget.
# All text som vi skriver i dokumentkroppen efter att ha flyttat ut ur taggen med piltangenterna kommer att använda detta teckensnitt.
tag.end_character_font.name = 'Arial Black'
# Som standard är detta falskt och att trycka på Enter medan du är inne i ett strukturerat dokumenttagg gör ingenting.
# När den är inställd på true kan vårt strukturerade dokumenttagg ha flera rader.
# Ställ in egenskapen "Multiline" till "false" för att endast tillåta innehållet
# för detta strukturerade dokumenttagg att sträcka sig över en enda rad.
# Ställ in egenskapen "Multiline" till "true" för att tillåta taggen att innehålla flera rader med innehåll.
tag.multiline = True
# Ställ in egenskapen "Appearance" till "SdtAppearance.Tags" för att visa taggar runt innehållet.
# Som standard visas strukturerat dokumenttagg som BoundingBox.
tag.appearance = aw.markup.SdtAppearance.TAGS
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(tag)
# Infoga en klon av vårt strukturerade dokumenttagg i ett nytt stycke.
tag_clone = tag.clone(True).as_structured_document_tag()
builder.insert_paragraph()
builder.insert_node(tag_clone)
# Använd metoden "RemoveSelfOnly" för att ta bort ett strukturerat dokumenttagg, samtidigt som dess innehåll behålls i dokumentet.
tag_clone.remove_self_only()
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.PlainText.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

