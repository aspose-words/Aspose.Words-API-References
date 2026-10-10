---
title: Run constructor
linktitle: Run constructor
articleTitle: Run constructor
second_title: Aspose.Words for Python
description: "aspose.words.Run constructor"
type: docs
weight: 10
url: /de/python-net/aspose.words/run/__init__/
---

## Run(doc) {#documentbase}

Initializes a new instance of the [Run](../) class.



```python
def __init__(self, doc: aspose.words.DocumentBase):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../documentbase/) | The owner document. |

### Remarks

When [Run](../) is created, it belongs to the specified document, but is not
yet part of the document and [Node.parent_node](../../node/parent_node/) is ``None``.

To append [Run](../) to the document use [CompositeNode.insert_after()](../../compositenode/insert_after/#node_node) or [CompositeNode.insert_before()](../../compositenode/insert_before/#node_node)
on the paragraph where you want the run inserted.




## Run(doc, text) {#documentbase_str}

Initializes a new instance of the **Run** class.



```python
def __init__(self, doc: aspose.words.DocumentBase, text: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../documentbase/) | The owner document. |
| text | str | The text of the run. |

### Remarks

When [Run](../) is created, it belongs to the specified document, but is not
yet part of the document and [Node.parent_node](../../node/parent_node/) is ``None``.

To append [Run](../) to the document use [CompositeNode.insert_after()](../../compositenode/insert_after/#node_node) or [CompositeNode.insert_before()](../../compositenode/insert_before/#node_node)
on the paragraph where you want the run inserted.




## Examples

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

Shows how to format a run of text using its font property.

```python
doc = aw.Document()
run = aw.Run(doc=doc, text='Hello world!')
font = run.font
font.name = 'Courier New'
font.size = 36
font.highlight_color = aspose.pydrawing.Color.yellow
doc.first_section.body.first_paragraph.append_child(run)
doc.save(file_name=ARTIFACTS_DIR + 'Font.CreateFormattedRun.docx')
```

## See Also

* module [aspose.words](../../)
* class [Run](../)

