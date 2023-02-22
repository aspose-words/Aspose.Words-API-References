---
title: Class HyphenationOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Settings.HyphenationOptions klas. Ermöglicht die Konfiguration von Silbentrennungsoptionen für Dokumente.
type: docs
weight: 5500
url: /de/net/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class

Ermöglicht die Konfiguration von Silbentrennungsoptionen für Dokumente.

```csharp
public class HyphenationOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [HyphenationOptions](hyphenationoptions/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AutoHyphenation](../../aspose.words.settings/hyphenationoptions/autohyphenation/) { get; set; } | Ruft den Wert ab oder legt ihn fest, der bestimmt, ob die automatische Silbentrennung für das Dokument aktiviert ist. Der Standardwert für diese Eigenschaft ist **FALSCH** . |
| [ConsecutiveHyphenLimit](../../aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/) { get; set; } | Ermittelt oder setzt die maximale Anzahl aufeinanderfolgender Zeilen, die mit Bindestrichen enden können. Der Standardwert für diese Eigenschaft ist 0. |
| [HyphenateCaps](../../aspose.words.settings/hyphenationoptions/hyphenatecaps/) { get; set; } | Erhält oder legt einen Wert fest, der bestimmt, ob Wörter, die ausschließlich in Großbuchstaben geschrieben sind, getrennt werden. Der Standardwert für diese Eigenschaft ist **Stimmt** . |
| [HyphenationZone](../../aspose.words.settings/hyphenationoptions/hyphenationzone/) { get; set; } | Ruft den Abstand in 1/20 Punkt vom rechten Rand ab oder legt ihn fest, innerhalb dessen keine Wörter getrennt werden sollen . Der Standardwert für diese Eigenschaft ist 360 (0,25 Zoll). |

### Beispiele

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

* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)


