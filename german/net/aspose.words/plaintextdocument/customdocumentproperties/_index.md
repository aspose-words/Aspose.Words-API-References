---
title: PlainTextDocument.CustomDocumentProperties
linktitle: CustomDocumentProperties
articleTitle: CustomDocumentProperties
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie in PlainTextDocument auf CustomDocumentProperties zugreifen, um die Dokumentenverwaltung und -anpassung zu verbessern. Entfesseln Sie das Potenzial Ihres Dokuments!
type: docs
weight: 30
url: /de/net/aspose.words/plaintextdocument/customdocumentproperties/
---
## PlainTextDocument.CustomDocumentProperties property

Ruft ab`CustomDocumentProperties` des Dokuments.

```csharp
public CustomDocumentProperties CustomDocumentProperties { get; }
```

## Beispiele

Zeigt, wie der Inhalt eines Microsoft Word-Dokuments im Klartext geladen und dann auf die benutzerdefinierten Eigenschaften des Originaldokuments zugegriffen wird.

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

### Siehe auch

* class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* class [PlainTextDocument](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
