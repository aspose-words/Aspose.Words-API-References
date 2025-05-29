---
title: FontInfo.IsTrueType
linktitle: IsTrueType
articleTitle: IsTrueType
second_title: Aspose.Words für .NET
description: Entdecken Sie die IsTrueType-Eigenschaft von FontInfo, die sicherstellt, dass Ihre Schriftart TrueType oder OpenType ist und so für höchste Qualität sorgt – perfekt für klare und skalierbare Designs.
type: docs
weight: 50
url: /de/net/aspose.words.fonts/fontinfo/istruetype/
---
## FontInfo.IsTrueType property

Gibt an, dass es sich bei dieser Schriftart um eine TrueType- oder OpenType-Schriftart und nicht um eine Raster- oder Vektorschriftart handelt. Standard ist`WAHR` .

```csharp
public bool IsTrueType { get; set; }
```

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

* class [FontInfo](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
