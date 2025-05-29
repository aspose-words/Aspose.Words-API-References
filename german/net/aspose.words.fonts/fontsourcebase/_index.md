---
title: FontSourceBase Class
linktitle: FontSourceBase
articleTitle: FontSourceBase
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.Fonts.FontSourceBase, die grundlegende abstrakte Klasse zum Definieren verschiedener Schriftquellen in Ihren Anwendungen. Verbessern Sie die Formatierung Ihrer Dokumente!
type: docs
weight: 3410
url: /de/net/aspose.words.fonts/fontsourcebase/
---
## FontSourceBase class

Dies ist eine abstrakte Basisklasse für die Klassen, die es dem Benutzer ermöglichen, verschiedene Schriftartquellen anzugeben.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Schriftarten](https://docs.aspose.com/words/net/working-with-fonts/) Dokumentationsartikel.

```csharp
public abstract class FontSourceBase
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Gibt die Priorität der Schriftartquelle zurück. |
| abstract [Type](../../aspose.words.fonts/fontsourcebase/type/) { get; } | Gibt den Typ der Schriftartquelle zurück. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Wird während der Verarbeitung der Schriftartquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungstreue führen kann. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Gibt eine Liste der über diese Quelle verfügbaren Schriftarten zurück. |

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
