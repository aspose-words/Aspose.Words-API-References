---
title: Run.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "Run.text property. Gets or sets the text of the run."
type: docs
weight: 50
url: /de/python-net/aspose.words/run/text/
---

## Run.text property

Gets or sets the text of the run.


```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

### Examples

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
* class [Run](../)

