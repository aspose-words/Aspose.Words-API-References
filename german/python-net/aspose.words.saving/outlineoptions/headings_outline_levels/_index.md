---
title: OutlineOptions.headings_outline_levels property
linktitle: headings_outline_levels property
articleTitle: headings_outline_levels property
second_title: Aspose.Words for Python
description: "OutlineOptions.headings_outline_levels property. Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the  document outline."
type: docs
weight: 70
url: /de/python-net/aspose.words.saving/outlineoptions/headings_outline_levels/
---

## OutlineOptions.headings_outline_levels property

Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the 
document outline.


```python
@property
def headings_outline_levels(self) -> int:
    ...

@headings_outline_levels.setter
def headings_outline_levels(self, value: int):
    ...

```

### Remarks

Specify 0 for no headings in the outline; specify 1 for one level of headings in the outline and so on.

Default is 0. Valid range is 0 to 9.




### Examples

Shows how to convert a whole document to PDF with three levels in the document outline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Fügen Sie Überschriften der Ebenen 1 bis 5 ein.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 1.2.1')
builder.writeln('Heading 1.2.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4
builder.writeln('Heading 1.2.2.1')
builder.writeln('Heading 1.2.2.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5
builder.writeln('Heading 1.2.2.2.1')
builder.writeln('Heading 1.2.2.2.2')
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
options = aw.saving.PdfSaveOptions()
# Das ausgegebene PDF-Dokument enthält ein Inhaltsverzeichnis, das eine Gliederung ist und die Überschriften im Dokumentkörper auflistet.
# Ein Klick auf einen Eintrag in diesem Inhaltsverzeichnis führt uns zur Position der jeweiligen Überschrift.
# Setzen Sie die "HeadingsOutlineLevels"-Eigenschaft auf "4", um alle Überschriften, deren Ebene über 4 liegt, aus der Gliederung auszuschließen.
options.outline_options.headings_outline_levels = 4
# Wenn ein Gliederungseintrag nachfolgende Einträge einer höheren Ebene zwischen sich und dem nächsten Eintrag derselben oder einer niedrigeren Ebene hat,
# erscheint links vom Eintrag ein Pfeil. Dieser Eintrag ist der "owner" mehrerer solcher "sub-entries".
# In unserem Dokument sind die Gliederungseinträge der 5. Überschriftenebene Untereinträge des zweiten Gliederungseintrags der 4. Ebene,
# Die Einträge der 4. und 5. Überschriftsebene sind Untereinträge des zweiten Eintrags der 3. Ebene und so weiter.
# Im Inhaltsverzeichnis können wir auf den Pfeil des Eintrags "owner" klicken, um alle Untereinträge ein- bzw. auszublenden.
# Setzen Sie die Eigenschaft "ExpandedOutlineLevels" auf "2", um automatisch alle Einträge der Überschriftsebene 2 und darunter im Inhaltsverzeichnis zu erweitern
# und blenden Sie alle Einträge der Ebene 3 und höher aus, wenn wir das Dokument öffnen.
options.outline_options.expanded_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExpandedOutlineLevels.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

