---
title: FontInfo.Panose
linktitle: Panose
articleTitle: Panose
second_title: Aspose.Words für .NET
description: Entdecken Sie die FontInfo PANOSE-Eigenschaft, mit der Sie ganz einfach die Schriftartklassifizierungsnummer abrufen oder festlegen können, um die Schriftartverwaltung und Designpräzision zu verbessern.
type: docs
weight: 70
url: /de/net/aspose.words.fonts/fontinfo/panose/
---
## FontInfo.Panose property

Ruft die PANOSE-Schriftklassifizierungsnummer ab oder legt sie fest.

```csharp
public byte[] Panose { get; set; }
```

## Bemerkungen

PANOSE ist eine kompakte 10-Byte-Beschreibung der wichtigsten visuellen Merkmale einer Schriftart, wie Kontrast, Stärke und Serifenstil. Die Ziffern stehen für Schriftfamilie, Serifenstil, Stärke, Proportion, Kontrast, Strichvariation, Armstil, Buchstabenform, Mittellinie und x-Höhe.

Kann sein`null`.

## Beispiele

Zeigt, wie Sie auf die Details jeder Schriftart in einem Dokument zugreifen und diese drucken können.

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

* class [FontInfo](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
