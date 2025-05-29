---
title: FontInfo.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words für .NET
description: Entdecken Sie die FontInfo-Name-Eigenschaft, um einfach auf Schriftnamen zuzugreifen und diese für eine verbesserte Typografie in Ihren Projekten zu verwenden.
type: docs
weight: 60
url: /de/net/aspose.words.fonts/fontinfo/name/
---
## FontInfo.Name property

Ruft den Namen der Schriftart ab.

```csharp
public string Name { get; }
```

## Bemerkungen

Kann nicht sein`null`. Kann eine leere Zeichenfolge sein.

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
