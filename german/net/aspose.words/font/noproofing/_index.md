---
title: Font.NoProofing
linktitle: NoProofing
articleTitle: NoProofing
second_title: Aspose.Words für .NET
description: Font NoProofing eigendom. True wenn die formatierten Zeichen nicht auf Rechtschreibung überprüft werden sollen in C#.
type: docs
weight: 280
url: /de/net/aspose.words/font/noproofing/
---
## Font.NoProofing property

True, wenn die formatierten Zeichen nicht auf Rechtschreibung überprüft werden sollen.

```csharp
public bool NoProofing { get; set; }
```

## Beispiele

Zeigt, wie Sie verhindern können, dass Text von Microsoft Word auf Rechtschreibung geprüft wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Normalerweise hebt Microsoft Word Rechtschreibfehler durch eine gezackte rote Unterstreichung hervor.
// Wir können das Flag „NoProofing“ deaktivieren, um einen Teil des Textes zu erstellen
// umgeht die Rechtschreibprüfung und deaktiviert sie vollständig.
builder.Font.NoProofing = true;

builder.Writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc.Save(ArtifactsDir + "Font.NoProofing.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
