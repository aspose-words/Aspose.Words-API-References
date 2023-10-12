---
title: Class FontInfo
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fonts.FontInfo klas. Gibt Informationen zu einer im Dokument verwendeten Schriftart an.
type: docs
weight: 2920
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
| [AltName](../../aspose.words.fonts/fontinfo/altname/) { get; set; } | Ruft den alternativen Namen für die Schriftart ab oder legt diesen fest. |
| [Charset](../../aspose.words.fonts/fontinfo/charset/) { get; set; } | Ruft den Zeichensatz für die Schriftart ab oder legt diesen fest. |
| [Family](../../aspose.words.fonts/fontinfo/family/) { get; set; } | Ruft die Schriftfamilie ab, zu der diese Schriftart gehört, oder legt diese fest. |
| [IsTrueType](../../aspose.words.fonts/fontinfo/istruetype/) { get; set; } | Gibt an, dass es sich bei dieser Schriftart um eine TrueType- oder OpenType-Schriftart und nicht um eine Raster- oder Vektorschriftart handelt. Die Standardeinstellung ist`WAHR` . |
| [Name](../../aspose.words.fonts/fontinfo/name/) { get; } | Ruft den Namen der Schriftart ab. |
| [Panose](../../aspose.words.fonts/fontinfo/panose/) { get; set; } | Ruft die Klassifizierungsnummer der PANOSE-Schriftart ab oder legt diese fest. |
| [Pitch](../../aspose.words.fonts/fontinfo/pitch/) { get; set; } | Die Tonhöhe gibt an, ob die Schriftart eine feste Tonhöhe, einen proportionalen Abstand oder eine Standardeinstellung hat. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetEmbeddedFont](../../aspose.words.fonts/fontinfo/getembeddedfont/)(EmbeddedFontFormat, EmbeddedFontStyle) | Ruft eine bestimmte eingebettete Schriftartdatei ab. |
| [GetEmbeddedFontAsOpenType](../../aspose.words.fonts/fontinfo/getembeddedfontasopentype/)(EmbeddedFontStyle) | Ruft eine eingebettete Schriftartdatei im OpenType-Format ab. Schriftarten im Embedded OpenType-Format werden in OpenType. konvertiert. |

### Bemerkungen

Sie erstellen keine Instanzen dieser Klasse direkt. Verwenden Sie die[`FontInfos`](../../aspose.words/documentbase/fontinfos/) Eigenschaft, um auf die Sammlung von Schriftarten zuzugreifen, die in einem Dokument definiert sind.

### Beispiele

Zeigt, wie die Details zu den in einem Dokument vorhandenen Schriftarten gedruckt werden.

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


