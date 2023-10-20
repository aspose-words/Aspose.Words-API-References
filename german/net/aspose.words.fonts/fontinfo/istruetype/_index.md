---
title: FontInfo.IsTrueType
linktitle: IsTrueType
articleTitle: IsTrueType
second_title: Aspose.Words für .NET
description: FontInfo IsTrueType eigendom. Gibt an dass es sich bei dieser Schriftart um eine TrueType oder OpenTypeSchriftart und nicht um eine Raster oder Vektorschriftart handelt. Die Standardeinstellung istWAHR  in C#.
type: docs
weight: 40
url: /de/net/aspose.words.fonts/fontinfo/istruetype/
---
## FontInfo.IsTrueType property

Gibt an, dass es sich bei dieser Schriftart um eine TrueType- oder OpenType-Schriftart und nicht um eine Raster- oder Vektorschriftart handelt. Die Standardeinstellung ist`WAHR` .

```csharp
public bool IsTrueType { get; set; }
```

## Beispiele

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

* class [FontInfo](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
