---
title: Node.get_text method
linktitle: get_text method
articleTitle: get_text method
second_title: Aspose.Words for Python
description: "Node.get_text method. Gets the text of this node and of all its children."
type: docs
weight: 450
url: /de/python-net/aspose.words/node/get_text/
---

## get_text() {#default}

Gets the text of this node and of all its children.


```python
def get_text(self):
    ...
```

### Remarks

The returned string includes all control and special characters as described in [ControlChar](../../controlchar/).




### Examples

Shows how to use control characters.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Füge Absätze mit Text mithilfe von DocumentBuilder ein.
builder.writeln('Hello world!')
builder.writeln('Hello again!')
# Die Umwandlung des Dokuments in Textform zeigt, dass Steuerzeichen
# einige der strukturellen Elemente des Dokuments darstellen, wie z. B. Seitenumbrüche.
self.assertEqual(f'Hello world!{aw.ControlChar.CR}' + f'Hello again!{aw.ControlChar.CR}' + aw.ControlChar.PAGE_BREAK, doc.get_text())
# Beim Konvertieren eines Dokuments in Zeichenkettenform,
# können wir einige der Steuerzeichen mit der Trim-Methode weglassen.
self.assertEqual(f'Hello world!{aw.ControlChar.CR}' + 'Hello again!', doc.get_text().strip())
```

Shows how to construct an Aspose.Words document by hand.

```python
doc = aw.Document()
# Ein leeres Dokument enthält einen Abschnitt, einen Body und einen Absatz.
# Rufen Sie die \"RemoveAllChildren\"-Methode auf, um alle diese Knoten zu entfernen,
# und erhalten einen Dokumentknoten ohne Kinder.
doc.remove_all_children()
# Dieses Dokument hat jetzt keine zusammengesetzten Kindknoten, zu denen wir Inhalte hinzufügen können.
# Wenn wir es bearbeiten möchten, müssen wir seine Knotensammlung neu befüllen.
# Zuerst erstellen Sie einen neuen Abschnitt und fügen ihn dann als Kind zum Wurzel-Dokumentknoten hinzu.
section = aw.Section(doc)
doc.append_child(section)
# Legen Sie einige Seiteneinrichtungs‑Eigenschaften für den Abschnitt fest.
section.page_setup.section_start = aw.SectionStart.NEW_PAGE
section.page_setup.paper_size = aw.PaperSize.LETTER
# Ein Abschnitt benötigt einen Body, der alle seine Inhalte enthält und anzeigt
# auf der Seite zwischen dem Header und Footer des Abschnitts.
body = aw.Body(doc)
section.append_child(body)
# Erstellen Sie einen Absatz, setzen Sie einige Formatierungseigenschaften und fügen Sie ihn dann als Kind zum Body hinzu.
para = aw.Paragraph(doc)
para.paragraph_format.style_name = 'Heading 1'
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
body.append_child(para)
# Schließlich fügen Sie etwas Inhalt zum Dokument hinzu. Erstellen Sie einen Run,
# setzen Sie sein Aussehen und seinen Inhalt und fügen Sie ihn dann als Kind zum Absatz hinzu.
run = aw.Run(doc=doc)
run.text = 'Hello World!'
run.font.color = aspose.pydrawing.Color.red
para.append_child(run)
self.assertEqual('Hello World!', doc.get_text().strip())
doc.save(file_name=ARTIFACTS_DIR + 'Section.CreateManually.docx')
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

