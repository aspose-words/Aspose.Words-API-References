---
title: PlainTextDocument.BuiltInDocumentProperties
second_title: Aspose.Words für .NET-API-Referenz
description: PlainTextDocument eigendom. Ruft abBuiltInDocumentProperties des Dokuments.
type: docs
weight: 20
url: /de/net/aspose.words/plaintextdocument/builtindocumentproperties/
---
## PlainTextDocument.BuiltInDocumentProperties property

Ruft ab`BuiltInDocumentProperties` des Dokuments.

```csharp
public BuiltInDocumentProperties BuiltInDocumentProperties { get; }
```

### Beispiele

Zeigt, wie man den Inhalt eines Microsoft Word-Dokuments im Klartext lädt und dann auf die integrierten Eigenschaften des Originaldokuments zugreift.

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
* namensraum [Aspose.Words](../../plaintextdocument/)
* Montage [Aspose.Words](../../../)


