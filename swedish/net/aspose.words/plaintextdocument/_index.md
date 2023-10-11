---
title: Class PlainTextDocument
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.PlainTextDocument klass. Tillåter att extrahera ren textrepresentation av dokumentets innehåll.
type: docs
weight: 4440
url: /sv/net/aspose.words/plaintextdocument/
---
## PlainTextDocument class

Tillåter att extrahera ren textrepresentation av dokumentets innehåll.

För att lära dig mer, besök[Arbeta med textdokument](https://docs.aspose.com/words/net/working-with-text-document/) dokumentationsartikel.

```csharp
public class PlainTextDocument
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [PlainTextDocument](plaintextdocument/#constructor)(Stream) | Skapar ett vanligt textdokument från en ström. Upptäcker automatiskt filformatet. |
| [PlainTextDocument](plaintextdocument/#constructor_2)(string) | Skapar ett vanligt textdokument från en fil. Upptäcker automatiskt filformatet. |
| [PlainTextDocument](plaintextdocument/#constructor_1)(Stream, LoadOptions) | Skapar ett vanligt textdokument från en ström. Tillåter att ange ytterligare alternativ såsom ett krypteringslösenord. |
| [PlainTextDocument](plaintextdocument/#constructor_3)(string, LoadOptions) | Skapar ett vanligt textdokument från en fil. Tillåter att ange ytterligare alternativ såsom ett krypteringslösenord. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BuiltInDocumentProperties](../../aspose.words/plaintextdocument/builtindocumentproperties/) { get; } | Blir[`BuiltInDocumentProperties`](./builtindocumentproperties/) av dokumentet. |
| [CustomDocumentProperties](../../aspose.words/plaintextdocument/customdocumentproperties/) { get; } | Blir[`CustomDocumentProperties`](./customdocumentproperties/) av dokumentet. |
| [Text](../../aspose.words/plaintextdocument/text/) { get; } | Får textinnehållet i dokumentet sammanfogat som en sträng. |

### Exempel

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


