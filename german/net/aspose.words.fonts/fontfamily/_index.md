---
title: Enum FontFamily
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fonts.FontFamily opsomming. steht für die Schriftfamilie.
type: docs
weight: 2730
url: /de/net/aspose.words.fonts/fontfamily/
---
## FontFamily enumeration

steht für die Schriftfamilie.

```csharp
public enum FontFamily
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Auto | `0` | Gibt einen generischen Familiennamen an. Dieser Name wird verwendet, wenn Informationen über eine Schriftart nicht vorhanden sind oder keine Rolle spielen. Die Standardschriftart wird verwendet. |
| Roman | `1` | Gibt eine proportionale Schriftart mit Serifen an. Ein Beispiel ist Times New Roman. |
| Swiss | `2` | Gibt eine Proportionalschrift ohne Serifen an. Ein Beispiel ist Arial. |
| Modern | `3` | Gibt eine Monospace-Schriftart mit oder ohne Serifen an. Monospace-Schriftarten sind normalerweise modern; Beispiele sind Pica, Elite und Courier New. |
| Script | `4` | Gibt eine Schriftart an, die wie Handschrift aussehen soll; Beispiele sind Script und Cursive. |
| Decorative | `5` | Gibt eine neuartige Schriftart an. Ein Beispiel ist Altenglisch. |

### Bemerkungen

Eine Fontfamilie ist ein Satz von Fonts mit gemeinsamen Strichstärken und Serifenmerkmalen.

### Beispiele

Zeigt, wie Sie auf Details jeder Schriftart in einem Dokument zugreifen und diese drucken können.

```csharp
Document doc = new Document(MyDir + "Document.docx");

IEnumerator<FontInfo> fontCollectionEnumerator = doc.FontInfos.GetEnumerator();
while (fontCollectionEnumerator.MoveNext())
{
    FontInfo fontInfo = fontCollectionEnumerator.Current;
    if (fontInfo != null)
    {
        Console.WriteLine("Font name: " + fontInfo.Name);

        // Alt-Namen sind normalerweise leer.
        Console.WriteLine("Alt name: " + fontInfo.AltName);
        Console.WriteLine("\t- Family: " + fontInfo.Family);
        Console.WriteLine("\t- " + (fontInfo.IsTrueType ? "Is TrueType" : "Is not TrueType"));
        Console.WriteLine("\t- Pitch: " + fontInfo.Pitch);
        Console.WriteLine("\t- Charset: " + fontInfo.Charset);
        Console.WriteLine("\t- Panose:");
        Console.WriteLine("\t\tFamily Kind: " + fontInfo.Panose[0]);
        Console.WriteLine("\t\tSerif Style: " + fontInfo.Panose[1]);
        Console.WriteLine("\t\tWeight: " + fontInfo.Panose[2]);
        Console.WriteLine("\t\tProportion: " + fontInfo.Panose[3]);
        Console.WriteLine("\t\tContrast: " + fontInfo.Panose[4]);
        Console.WriteLine("\t\tStroke Variation: " + fontInfo.Panose[5]);
        Console.WriteLine("\t\tArm Style: " + fontInfo.Panose[6]);
        Console.WriteLine("\t\tLetterform: " + fontInfo.Panose[7]);
        Console.WriteLine("\t\tMidline: " + fontInfo.Panose[8]);
        Console.WriteLine("\t\tX-Height: " + fontInfo.Panose[9]);
    }
}
```

### Siehe auch

* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)


