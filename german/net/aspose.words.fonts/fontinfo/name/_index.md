---
title: FontInfo.Name
second_title: Aspose.Words für .NET-API-Referenz
description: FontInfo eigendom. Ruft den Namen der Schriftart ab.
type: docs
weight: 50
url: /de/net/aspose.words.fonts/fontinfo/name/
---
## FontInfo.Name property

Ruft den Namen der Schriftart ab.

```csharp
public string Name { get; }
```

### Bemerkungen

Kann nicht sein`Null`. Kann eine leere Zeichenfolge sein.

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

* class [FontInfo](../)
* namensraum [Aspose.Words.Fonts](../../fontinfo/)
* Montage [Aspose.Words](../../../)


