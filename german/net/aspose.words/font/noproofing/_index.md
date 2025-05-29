---
title: Font.NoProofing
linktitle: NoProofing
articleTitle: NoProofing
second_title: Aspose.Words für .NET
description: Entdecken Sie Font NoProofing. Vermeiden Sie die Rechtschreibprüfung formatierten Textes für klarere Designs. Optimieren Sie Ihre Dokumente mit Präzision und Professionalität!
type: docs
weight: 280
url: /de/net/aspose.words/font/noproofing/
---
## Font.NoProofing property

Wahr, wenn für die formatierten Zeichen keine Rechtschreibprüfung durchgeführt werden soll.

```csharp
public bool NoProofing { get; set; }
```

## Beispiele

Zeigt, wie Sie die Rechtschreibprüfung von Text durch Microsoft Word verhindern können.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Normalerweise hebt Microsoft Word Rechtschreibfehler mit einer gezackten roten Unterstreichung hervor.
// Wir können das Flag „NoProofing“ deaktivieren, um einen Textabschnitt zu erstellen, der
// umgeht die Rechtschreibprüfung und deaktiviert sie vollständig.
builder.Font.NoProofing = true;

builder.Writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc.Save(ArtifactsDir + "Font.NoProofing.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
