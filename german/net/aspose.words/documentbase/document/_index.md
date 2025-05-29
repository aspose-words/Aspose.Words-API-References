---
title: DocumentBase.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words für .NET
description: Entdecken Sie die Funktionen von DocumentBase für eine effiziente Dokumentenverwaltung. Profitieren Sie von nahtlosem Zugriff und optimieren Sie Ihren Workflow noch heute!
type: docs
weight: 20
url: /de/net/aspose.words/documentbase/document/
---
## DocumentBase.Document property

Ruft diese Instanz ab.

```csharp
public override DocumentBase Document { get; }
```

## Beispiele

Zeigt, wie man ein einfaches Dokument erstellt.

```csharp
Document doc = new Document();

// Neue Dokumentobjekte werden standardmäßig mit dem minimalen Satz an Knoten geliefert
// erforderlich, um mit dem Hinzufügen von Inhalten wie Text und Formen zu beginnen: ein Abschnitt, ein Textkörper und ein Absatz.
doc.AppendChild(new Section(doc))
    .AppendChild(new Body(doc))
    .AppendChild(new Paragraph(doc))
    .AppendChild(new Run(doc, "Hello world!"));
```

### Siehe auch

* class [DocumentBase](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
