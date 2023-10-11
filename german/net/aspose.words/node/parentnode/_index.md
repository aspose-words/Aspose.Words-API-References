---
title: Node.ParentNode
second_title: Aspose.Words für .NET-API-Referenz
description: Node eigendom. Ruft das unmittelbare übergeordnete Element dieses Knotens ab.
type: docs
weight: 60
url: /de/net/aspose.words/node/parentnode/
---
## Node.ParentNode property

Ruft das unmittelbare übergeordnete Element dieses Knotens ab.

```csharp
public CompositeNode ParentNode { get; }
```

### Bemerkungen

Wenn ein Knoten gerade erst erstellt und noch nicht zum Baum hinzugefügt wurde, oder wenn er aus dem Baum entfernt wurde, ist es der übergeordnete Knoten`Null`.

### Beispiele

Zeigt, wie auf den übergeordneten Knoten eines Knotens zugegriffen wird.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Einen untergeordneten Run-Knoten an den ersten Absatz des Dokuments anhängen.
Run run = new Run(doc, "Hello world!");
para.AppendChild(run);

// Der Absatz ist der übergeordnete Knoten des Ausführungsknotens. Wir können diese Abstammung verfolgen
// bis zum Dokumentknoten, der die Wurzel des Knotenbaums des Dokuments darstellt.
Assert.AreEqual(para, run.ParentNode);
Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual(doc.FirstSection, doc.FirstSection.Body.ParentNode);
Assert.AreEqual(doc, doc.FirstSection.ParentNode);
```

Zeigt, wie ein Knoten erstellt und sein besitzendes Dokument festgelegt wird.

```csharp
Document doc = new Document();
Paragraph para = new Paragraph(doc);
para.AppendChild(new Run(doc, "Hello world!"));

// Wir haben diesen Absatz noch nicht als untergeordnetes Element an einen zusammengesetzten Knoten angehängt.
Assert.IsNull(para.ParentNode);

// Wenn ein Knoten ein geeigneter untergeordneter Knotentyp eines anderen zusammengesetzten Knotens ist,
// Wir können es nur dann als Kind anhängen, wenn beide Knoten das gleiche Besitzerdokument haben.
// Das Eigentümerdokument ist das Dokument, das wir an den Konstruktor des Knotens übergeben haben.
// Wir haben diesen Absatz nicht an das Dokument angehängt, daher enthält das Dokument seinen Text nicht.
Assert.AreEqual(para.Document, doc);
Assert.AreEqual(string.Empty, doc.GetText().Trim());

// Da das Dokument Eigentümer dieses Absatzes ist, können wir einen seiner Stile auf den Inhalt des Absatzes anwenden.
para.ParagraphFormat.Style = doc.Styles["Heading 1"];

// Fügen Sie diesen Knoten zum Dokument hinzu und überprüfen Sie dann seinen Inhalt.
doc.FirstSection.Body.AppendChild(para);

Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Siehe auch

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* namensraum [Aspose.Words](../../node/)
* Montage [Aspose.Words](../../../)


