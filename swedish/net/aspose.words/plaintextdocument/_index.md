---
title: PlainTextDocument Class
linktitle: PlainTextDocument
articleTitle: PlainTextDocument
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.PlainTextDocument för att enkelt extrahera och använda klartext från dina dokument för förbättrad läsbarhet och bearbetning.
type: docs
weight: 5170
url: /sv/net/aspose.words/plaintextdocument/
---
## PlainTextDocument class

Gör det möjligt att extrahera en representation av dokumentets innehåll i klartext.

För att lära dig mer, besök[Arbeta med textdokument](https://docs.aspose.com/words/net/working-with-text-document/) dokumentationsartikel.

```csharp
public class PlainTextDocument
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [PlainTextDocument](plaintextdocument/#constructor)(*Stream*) | Skapar ett vanligt textdokument från en ström. Identifierar automatiskt filformatet. |
| [PlainTextDocument](plaintextdocument/#constructor_2)(*string*) | Skapar ett vanligt textdokument från en fil. Identifierar automatiskt filformatet. |
| [PlainTextDocument](plaintextdocument/#constructor_1)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Skapar ett vanligt textdokument från en ström. Gör det möjligt att ange ytterligare alternativ, till exempel ett krypteringslösenord. |
| [PlainTextDocument](plaintextdocument/#constructor_3)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Skapar ett vanligt textdokument från en fil. Gör det möjligt att ange ytterligare alternativ, till exempel ett krypteringslösenord. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BuiltInDocumentProperties](../../aspose.words/plaintextdocument/builtindocumentproperties/) { get; } | Får[`BuiltInDocumentProperties`](./builtindocumentproperties/) av dokumentet. |
| [CustomDocumentProperties](../../aspose.words/plaintextdocument/customdocumentproperties/) { get; } | Får[`CustomDocumentProperties`](./customdocumentproperties/) av dokumentet. |
| [Text](../../aspose.words/plaintextdocument/text/) { get; } | Hämtar textinnehållet i dokumentet sammanfogat som en sträng. |

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

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
