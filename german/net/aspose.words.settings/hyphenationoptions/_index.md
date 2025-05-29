---
title: HyphenationOptions Class
linktitle: HyphenationOptions
articleTitle: HyphenationOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Settings.HyphenationOptions, um die Silbentrennungseinstellungen für Ihre Dokumente mühelos anzupassen und die Textdarstellung zu verbessern.
type: docs
weight: 6620
url: /de/net/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class

Ermöglicht die Konfiguration der Silbentrennungsoptionen für Dokumente.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Silbentrennung](https://docs.aspose.com/words/net/working-with-hyphenation/) Dokumentationsartikel.

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
| [AutoHyphenation](../../aspose.words.settings/hyphenationoptions/autohyphenation/) { get; set; } | Ruft den Wert ab oder legt ihn fest, der bestimmt, ob die automatische Silbentrennung für das Dokument aktiviert ist. Der Standardwert für diese Eigenschaft ist`FALSCH` . |
| [ConsecutiveHyphenLimit](../../aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/) { get; set; } | Ruft die maximale Anzahl aufeinanderfolgender Zeilen ab, die mit Bindestrichen enden können, oder legt diese fest. Der Standardwert für diese Eigenschaft ist 0. |
| [HyphenateCaps](../../aspose.words.settings/hyphenationoptions/hyphenatecaps/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob Wörter, die in Großbuchstaben geschrieben sind, mit Bindestrichen getrennt werden. Der Standardwert für diese Eigenschaft ist`WAHR` . |
| [HyphenationZone](../../aspose.words.settings/hyphenationoptions/hyphenationzone/) { get; set; } | Ruft den Abstand in 1/20 Punkt vom rechten Rand ab oder legt ihn fest, innerhalb dessen Wörter nicht getrennt werden sollen. Der Standardwert für diese Eigenschaft ist 360 (0,25 Zoll). |

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

* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)
