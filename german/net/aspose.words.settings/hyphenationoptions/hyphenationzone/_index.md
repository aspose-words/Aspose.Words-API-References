---
title: HyphenationOptions.HyphenationZone
linktitle: HyphenationZone
articleTitle: HyphenationZone
second_title: Aspose.Words für .NET
description: Optimieren Sie das Textlayout mit der Eigenschaft „HyphenationZone“. Steuern Sie den Silbentrennungsabstand vom rechten Rand für übersichtlichere, professionelle Dokumente.
type: docs
weight: 50
url: /de/net/aspose.words.settings/hyphenationoptions/hyphenationzone/
---
## HyphenationOptions.HyphenationZone property

Ruft den Abstand in 1/20 Punkt vom rechten Rand ab oder legt ihn fest, innerhalb dessen Wörter nicht getrennt werden sollen. Der Standardwert für diese Eigenschaft ist 360 (0,25 Zoll).

```csharp
public int HyphenationZone { get; set; }
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
