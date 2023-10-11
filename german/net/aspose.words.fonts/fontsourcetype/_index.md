---
title: Enum FontSourceType
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fonts.FontSourceType opsomming. Gibt den Typ einer Schriftartquelle an.
type: docs
weight: 2990
url: /de/net/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enumeration

Gibt den Typ einer Schriftartquelle an.

```csharp
public enum FontSourceType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| FontFile | `0` | A[`FileFontSource`](../filefontsource/) Objekt, das eine einzelne Schriftartdatei darstellt. |
| FontsFolder | `1` | A[`FolderFontSource`](../folderfontsource/) Objekt, das einen Ordner mit Schriftartdateien darstellt. |
| MemoryFont | `2` | A[`MemoryFontSource`](../memoryfontsource/) Objekt, das eine einzelne Schriftart im Speicher darstellt. |
| SystemFonts | `3` | A[`SystemFontSource`](../systemfontsource/) Objekt, das alle auf dem System installierten Schriftarten darstellt. |
| FontStream | `4` | A[`StreamFontSource`](../streamfontsource/) Objekt, das einen Stream mit Schriftartdaten darstellt. |

### Beispiele

Zeigt, wie eine Schriftartendatei im lokalen Dateisystem als Schriftartenquelle verwendet wird.

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


