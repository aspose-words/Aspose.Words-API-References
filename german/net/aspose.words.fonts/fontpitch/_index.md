---
title: Enum FontPitch
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fonts.FontPitch opsomming. Repräsentiert den Schriftabstand.
type: docs
weight: 2780
url: /de/net/aspose.words.fonts/fontpitch/
---
## FontPitch enumeration

Repräsentiert den Schriftabstand.

```csharp
public enum FontPitch
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Default | `0` | Gibt an, dass keine Informationen über die Tonhöhe einer Schriftart verfügbar sind. |
| Fixed | `1` | Gibt an, dass es sich um eine Schriftart mit fester Breite handelt. |
| Variable | `2` | Gibt an, dass es sich um eine Schriftart mit proportionaler Breite handelt. |

### Bemerkungen

Die Teilung gibt an, ob die Schriftart eine feste Teilung hat, proportionale Abstände aufweist oder auf einer Standardeinstellung beruht.

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


