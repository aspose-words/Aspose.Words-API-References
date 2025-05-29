---
title: Node.ParentNode
linktitle: ParentNode
articleTitle: ParentNode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Node ParentNode-Eigenschaft, um einfach auf den unmittelbar übergeordneten Knoten eines beliebigen Knotens zuzugreifen und so die Effizienz Ihrer Webentwicklung und die Übersichtlichkeit Ihres Codes zu verbessern.
type: docs
weight: 60
url: /de/net/aspose.words/node/parentnode/
---
## Node.ParentNode property

Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab.

```csharp
public CompositeNode ParentNode { get; }
```

## Bemerkungen

Wenn ein Knoten gerade erstellt und noch nicht zum Baum hinzugefügt wurde, oder wenn er aus dem Baum entfernt wurde, ist der übergeordnete Knoten`null`.

## Beispiele

Zeigt, wie auf den übergeordneten Knoten eines Knotens zugegriffen wird.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Fügen Sie dem ersten Absatz des Dokuments einen untergeordneten Run-Knoten hinzu.
Run run = new Run(doc, "Hello world!");
para.AppendChild(run);

// Der Absatz ist der übergeordnete Knoten des Run-Knotens. Wir können diese Herkunft verfolgen
// bis zum Dokumentknoten, der die Wurzel des Knotenbaums des Dokuments ist.
Assert.AreEqual(para, run.ParentNode);
Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual(doc.FirstSection, doc.FirstSection.Body.ParentNode);
Assert.AreEqual(doc, doc.FirstSection.ParentNode);
```

Zeigt, wie ein Knoten erstellt und sein zugehöriges Dokument festgelegt wird.

```csharp
Document doc = new Document();
Paragraph para = new Paragraph(doc);
para.AppendChild(new Run(doc, "Hello world!"));

// Wir haben diesen Absatz noch keinem zusammengesetzten Knoten als untergeordnetes Element angehängt.
Assert.IsNull(para.ParentNode);

// Wenn ein Knoten ein geeigneter untergeordneter Knotentyp eines anderen zusammengesetzten Knotens ist,
// wir können es nur als untergeordnetes Element anhängen, wenn beide Knoten dasselbe Eigentümerdokument haben.
// Das Eigentümerdokument ist das Dokument, das wir an den Konstruktor des Knotens übergeben haben.
// Wir haben diesen Absatz nicht an das Dokument angehängt, daher enthält das Dokument seinen Text nicht.
Assert.AreEqual(para.Document, doc);
Assert.AreEqual(string.Empty, doc.GetText().Trim());

// Da das Dokument diesen Absatz besitzt, können wir einen seiner Stile auf den Inhalt des Absatzes anwenden.
para.ParagraphFormat.Style = doc.Styles["Heading 1"];

// Fügen Sie diesen Knoten zum Dokument hinzu und überprüfen Sie dann seinen Inhalt.
doc.FirstSection.Body.AppendChild(para);

Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Siehe auch

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
