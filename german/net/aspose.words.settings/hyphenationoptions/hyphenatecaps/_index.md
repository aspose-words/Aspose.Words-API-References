---
title: HyphenationOptions.HyphenateCaps
linktitle: HyphenateCaps
articleTitle: HyphenateCaps
second_title: Aspose.Words für .NET
description: HyphenationOptions HyphenateCaps eigendom. Ruft den Wert ab oder legt diesen fest der bestimmt ob in Großbuchstaben geschriebene Wörter getrennt werden. Der Standardwert für diese Eigenschaft istWAHR  in C#.
type: docs
weight: 40
url: /de/net/aspose.words.settings/hyphenationoptions/hyphenatecaps/
---
## HyphenationOptions.HyphenateCaps property

Ruft den Wert ab oder legt diesen fest, der bestimmt, ob in Großbuchstaben geschriebene Wörter getrennt werden. Der Standardwert für diese Eigenschaft ist`WAHR` .

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
