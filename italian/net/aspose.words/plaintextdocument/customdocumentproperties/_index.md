---
title: PlainTextDocument.CustomDocumentProperties
second_title: Aspose.Words per .NET API Reference
description: PlainTextDocument proprietà. OttieneCustomDocumentProperties del documento.
type: docs
weight: 30
url: /it/net/aspose.words/plaintextdocument/customdocumentproperties/
---
## PlainTextDocument.CustomDocumentProperties property

Ottiene`CustomDocumentProperties` del documento.

```csharp
public CustomDocumentProperties CustomDocumentProperties { get; }
```

### Esempi

Mostra come caricare il contenuto di un documento di Microsoft Word in testo normale e quindi accedere alle proprietà personalizzate del documento originale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
doc.CustomDocumentProperties.Add("Location of writing", "123 Main St, London, UK");

doc.Save(ArtifactsDir + "PlainTextDocument.CustomDocumentProperties.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.CustomDocumentProperties.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
Assert.AreEqual("123 Main St, London, UK", plaintext.CustomDocumentProperties["Location of writing"].Value);
```

### Guarda anche

* class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* class [PlainTextDocument](../)
* spazio dei nomi [Aspose.Words](../../plaintextdocument/)
* assemblea [Aspose.Words](../../../)


