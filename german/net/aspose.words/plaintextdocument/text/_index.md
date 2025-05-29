---
title: PlainTextDocument.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words für .NET
description: Greifen Sie auf die Texteigenschaft des PlainTextDocument zu, um den Inhalt des Dokuments als einzelne Zeichenfolge abzurufen und so Ihre Datenverarbeitung und -analyse zu verbessern.
type: docs
weight: 40
url: /de/net/aspose.words/plaintextdocument/text/
---
## PlainTextDocument.Text property

Ruft den Textinhalt des Dokuments als Zeichenfolge ab.

```csharp
public string Text { get; }
```

## Beispiele

Zeigt, wie der Inhalt eines Microsoft Word-Dokuments im Klartext geladen wird.

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Siehe auch

* class [PlainTextDocument](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
