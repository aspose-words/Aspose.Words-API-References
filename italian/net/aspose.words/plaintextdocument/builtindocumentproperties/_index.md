---
title: PlainTextDocument.BuiltInDocumentProperties
second_title: Aspose.Words per .NET API Reference
description: PlainTextDocument proprietà. OttieneBuiltInDocumentProperties del documento.
type: docs
weight: 20
url: /it/net/aspose.words/plaintextdocument/builtindocumentproperties/
---
## PlainTextDocument.BuiltInDocumentProperties property

Ottiene`BuiltInDocumentProperties` del documento.

```csharp
public BuiltInDocumentProperties BuiltInDocumentProperties { get; }
```

### Esempi

Mostra come caricare il contenuto di un documento di Microsoft Word in testo normale e quindi accedere alle proprietà integrate del documento originale.

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

### Guarda anche

* class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* class [PlainTextDocument](../)
* spazio dei nomi [Aspose.Words](../../plaintextdocument/)
* assemblea [Aspose.Words](../../../)


