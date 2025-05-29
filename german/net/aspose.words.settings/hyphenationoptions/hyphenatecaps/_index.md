---
title: HyphenationOptions.HyphenateCaps
linktitle: HyphenateCaps
articleTitle: HyphenateCaps
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „HyphenateCaps“ in „HyphenationOptions“. Steuern Sie die Silbentrennung für Wörter in Großbuchstaben ganz einfach – die Standardeinstellung ist „true“. Optimieren Sie Ihren Text noch heute!
type: docs
weight: 40
url: /de/net/aspose.words.settings/hyphenationoptions/hyphenatecaps/
---
## HyphenationOptions.HyphenateCaps property

Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob Wörter, die in Großbuchstaben geschrieben sind, mit Bindestrichen getrennt werden. Der Standardwert für diese Eigenschaft ist`WAHR` .

```csharp
public bool HyphenateCaps { get; set; }
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

* class [HyphenationOptions](../)
* namensraum [Aspose.Words.Settings](../../../aspose.words.settings/)
* Montage [Aspose.Words](../../../)
