---
title: FontInfo Class
linktitle: FontInfo
articleTitle: FontInfo
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fonts.FontInfo, Ihren Schlüssel zu detaillierten Schriftarteinblicken für Dokumente, die die Textqualität und visuelle Attraktivität verbessern.
type: docs
weight: 3350
url: /de/net/aspose.words.fonts/fontinfo/
---
## FontInfo class

Gibt Informationen zu einer im Dokument verwendeten Schriftart an.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Schriftarten](https://docs.aspose.com/words/net/working-with-fonts/) Dokumentationsartikel.

```csharp
public class FontInfo
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AltName](../../aspose.words.fonts/fontinfo/altname/) { get; set; } | Ruft den alternativen Namen für die Schriftart ab oder legt ihn fest. |
| [Charset](../../aspose.words.fonts/fontinfo/charset/) { get; set; } | Ruft den Zeichensatz für die Schriftart ab oder legt ihn fest. |
| [EmbeddingLicensingRights](../../aspose.words.fonts/fontinfo/embeddinglicensingrights/) { get; } | Ruft die Lizenzrechte für eingebettete Schriftarten ab. |
| [Family](../../aspose.words.fonts/fontinfo/family/) { get; set; } | Ruft die Schriftfamilie ab oder legt sie fest, zu der diese Schriftart gehört. |
| [IsTrueType](../../aspose.words.fonts/fontinfo/istruetype/) { get; set; } | Gibt an, dass es sich bei dieser Schriftart um eine TrueType- oder OpenType-Schriftart und nicht um eine Raster- oder Vektorschriftart handelt. Standard ist`WAHR` . |
| [Name](../../aspose.words.fonts/fontinfo/name/) { get; } | Ruft den Namen der Schriftart ab. |
| [Panose](../../aspose.words.fonts/fontinfo/panose/) { get; set; } | Ruft die PANOSE-Schriftklassifizierungsnummer ab oder legt sie fest. |
| [Pitch](../../aspose.words.fonts/fontinfo/pitch/) { get; set; } | Die Tonhöhe gibt an, ob die Schriftart eine feste Tonhöhe hat, proportional verteilt ist oder auf einer Standardeinstellung basiert. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetEmbeddedFont](../../aspose.words.fonts/fontinfo/getembeddedfont/)(*[EmbeddedFontFormat](../embeddedfontformat/), [EmbeddedFontStyle](../embeddedfontstyle/)*) | Ruft eine bestimmte eingebettete Schriftartdatei ab. |
| [GetEmbeddedFontAsOpenType](../../aspose.words.fonts/fontinfo/getembeddedfontasopentype/)(*[EmbeddedFontStyle](../embeddedfontstyle/)*) | Ruft eine eingebettete Schriftdatei im OpenType-Format ab. Schriftarten im Embedded OpenType-Format werden in OpenType konvertiert. |

## Bemerkungen

Sie erstellen keine Instanzen dieser Klasse direkt. Verwenden Sie die[`FontInfos`](../../aspose.words/documentbase/fontinfos/) -Eigenschaft, um auf die in einem Dokument definierte Sammlung von fonts zuzugreifen.

## Beispiele

Zeigt, wie Sie die Details der in einem Dokument vorhandenen Schriftarten ausdrucken.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Alle verwendeten und nicht verwendeten Schriftarten im Dokument drucken.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### Siehe auch

* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)
