---
title: BuiltInDocumentProperties
second_title: Aspose.Words för .NET API Referens
description: BlirBuiltInDocumentPropertiesaspose.words/plaintextdocument/builtindocumentproperties av dokumentet.
type: docs
weight: 20
url: /sv/net/aspose.words/plaintextdocument/builtindocumentproperties/
---
## PlainTextDocument.BuiltInDocumentProperties property

Blir`BuiltInDocumentProperties` av dokumentet.

```csharp
public BuiltInDocumentProperties BuiltInDocumentProperties { get; }
```

### Exempel

Visar hur man laddar innehållet i ett Microsoft Word-dokument i klartext och sedan kommer åt originaldokumentets inbyggda egenskaper.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
doc.BuiltInDocumentProperties.Author = "John Doe";

doc.Save(ArtifactsDir + "PlainTextDocument.BuiltInProperties.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.BuiltInProperties.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
Assert.AreEqual("John Doe", plaintext.BuiltInDocumentProperties.Author);
```

### Se även

* class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties)
* class [PlainTextDocument](../../plaintextdocument)
* namnutrymme [Aspose.Words](../../plaintextdocument)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
