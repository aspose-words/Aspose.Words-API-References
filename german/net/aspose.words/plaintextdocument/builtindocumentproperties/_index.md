---
title: PlainTextDocument.BuiltInDocumentProperties
linktitle: BuiltInDocumentProperties
articleTitle: BuiltInDocumentProperties
second_title: Aspose.Words für .NET
description: Entdecken Sie die BuiltInDocumentProperties-Eigenschaft von PlainTextDocument, um einfach auf wichtige Dokumentmetadaten zuzugreifen und diese zu verwalten und so die Dokumentorganisation zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words/plaintextdocument/builtindocumentproperties/
---
## PlainTextDocument.BuiltInDocumentProperties property

Ruft ab`BuiltInDocumentProperties` des Dokuments.

```csharp
public BuiltInDocumentProperties BuiltInDocumentProperties { get; }
```

## Beispiele

Zeigt, wie der Inhalt eines Microsoft Word-Dokuments im Klartext geladen und dann auf die integrierten Eigenschaften des Originaldokuments zugegriffen wird.

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

### Siehe auch

* class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* class [PlainTextDocument](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
