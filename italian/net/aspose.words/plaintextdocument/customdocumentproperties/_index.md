---
title: PlainTextDocument.CustomDocumentProperties
linktitle: CustomDocumentProperties
articleTitle: CustomDocumentProperties
second_title: Aspose.Words per .NET
description: Scopri come accedere a CustomDocumentProperties in PlainTextDocument per una gestione e una personalizzazione ottimizzate dei documenti. Sfrutta il potenziale del tuo documento!
type: docs
weight: 30
url: /it/net/aspose.words/plaintextdocument/customdocumentproperties/
---
## PlainTextDocument.CustomDocumentProperties property

Ottiene`CustomDocumentProperties` del documento.

```csharp
public CustomDocumentProperties CustomDocumentProperties { get; }
```

## Esempi

Mostra come caricare il contenuto di un documento Microsoft Word in testo normale e quindi accedere alle proprietà personalizzate del documento originale.

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
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
