---
title: Node.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words für .NET
description: Node Document eigendom. Ruft das Dokument ab zu dem dieser Knoten gehört in C#.
type: docs
weight: 20
url: /de/net/aspose.words/node/document/
---
## Node.Document property

Ruft das Dokument ab, zu dem dieser Knoten gehört.

```csharp
public virtual DocumentBase Document { get; }
```

## Bemerkungen

Der Knoten gehört immer zu einem Dokument, auch wenn er gerade erst erstellt und noch nicht zum Baum hinzugefügt wurde, oder wenn er aus dem Baum entfernt wurde.

## Beispiele

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

* class [DocumentBase](../../documentbase/)
* class [Node](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
