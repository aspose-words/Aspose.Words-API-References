---
title: PlainTextDocument.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words för .NET
description: PlainTextDocument Text fast egendom. Får textinnehållet i dokumentet sammanfogat som en sträng i C#.
type: docs
weight: 40
url: /sv/net/aspose.words/plaintextdocument/text/
---
## PlainTextDocument.Text property

Får textinnehållet i dokumentet sammanfogat som en sträng.

```csharp
public string Text { get; }
```

## Exempel

Visar hur man laddar innehållet i ett Microsoft Word-dokument i klartext.

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Se även

* class [PlainTextDocument](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
