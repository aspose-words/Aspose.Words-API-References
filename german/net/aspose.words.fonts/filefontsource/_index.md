---
title: Class FileFontSource
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fonts.FileFontSource klas. Stellt die einzelne TrueTypeSchriftartdatei dar die im Dateisystem gespeichert ist.
type: docs
weight: 2690
url: /de/net/aspose.words.fonts/filefontsource/
---
## FileFontSource class

Stellt die einzelne TrueType-Schriftartdatei dar, die im Dateisystem gespeichert ist.

```csharp
public class FileFontSource : FontSourceBase
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FileFontSource](filefontsource/#constructor)(string) | Ctor. |
| [FileFontSource](filefontsource/#constructor_1)(string, int) | Ctor. |
| [FileFontSource](filefontsource/#constructor_2)(string, int, string) | Ctor. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/filefontsource/cachekey/) { get; } | Der Schlüssel dieser Quelle im Cache. |
| [FilePath](../../aspose.words.fonts/filefontsource/filepath/) { get; } | Pfad zur Schriftdatei. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Gibt die Priorität der Schriftquelle zurück. |
| override [Type](../../aspose.words.fonts/filefontsource/type/) { get; } | Gibt den Typ der Schriftartquelle zurück. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Wird während der Verarbeitung der Schriftartquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungstreue führen kann. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Gibt eine Liste der Schriftarten zurück, die über diese Quelle verfügbar sind. |

### Beispiele

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

* class [FontSourceBase](../fontsourcebase/)
* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)


