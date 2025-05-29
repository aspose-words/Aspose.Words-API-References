---
title: Document.HyphenationOptions
linktitle: HyphenationOptions
articleTitle: HyphenationOptions
second_title: Aspose.Words für .NET
description: Erkunden Sie die Eigenschaft „Document HyphenationOptions“, um die Silbentrennungseinstellungen anzupassen und so die Lesbarkeit zu verbessern und die Präsentation Ihres Dokuments zu verbessern.
type: docs
weight: 220
url: /de/net/aspose.words/document/hyphenationoptions/
---
## Document.HyphenationOptions property

Bietet Zugriff auf Dokument-Silbentrennungsoptionen.

```csharp
public HyphenationOptions HyphenationOptions { get; }
```

## Beispiele

Zeigt, wie die automatische Silbentrennung konfiguriert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.HyphenationOptions.AutoHyphenation = true;
doc.HyphenationOptions.ConsecutiveHyphenLimit = 2;
doc.HyphenationOptions.HyphenationZone = 720;
doc.HyphenationOptions.HyphenateCaps = true;

doc.Save(ArtifactsDir + "Document.HyphenationOptions.docx");
```

### Siehe auch

* class [HyphenationOptions](../../../aspose.words.settings/hyphenationoptions/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
