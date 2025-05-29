---
title: FontSourceType Enum
linktitle: FontSourceType
articleTitle: FontSourceType
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.Fonts.FontSourceType Enumeration für effizientes Schriftquellenmanagement. Optimieren Sie Ihre Dokumentverarbeitung mit flexiblen Schriftartenoptionen.
type: docs
weight: 3420
url: /de/net/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enumeration

Gibt den Typ der Schriftartquelle an.

```csharp
public enum FontSourceType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| FontFile | `0` | A[`FileFontSource`](../filefontsource/) Objekt, das eine einzelne Schriftartdatei darstellt. |
| FontsFolder | `1` | A[`FolderFontSource`](../folderfontsource/) Objekt, das einen Ordner mit Schriftdateien darstellt. |
| MemoryFont | `2` | A[`MemoryFontSource`](../memoryfontsource/) Objekt, das eine einzelne Schriftart im Speicher darstellt. |
| SystemFonts | `3` | A[`SystemFontSource`](../systemfontsource/) Objekt, das alle im System installierten Schriftarten darstellt. |
| FontStream | `4` | A[`StreamFontSource`](../streamfontsource/) Objekt, das einen Stream mit Schriftdaten darstellt. |

## Beispiele

Zeigt, wie eine Schriftartdatei im lokalen Dateisystem als Schriftartquelle verwendet wird.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### Siehe auch

* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)
