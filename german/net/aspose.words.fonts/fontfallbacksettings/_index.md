---
title: Class FontFallbackSettings
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fonts.FontFallbackSettings klas. Gibt die Einstellungen für den FallbackMechanismus für Schriftarten an.
type: docs
weight: 2720
url: /de/net/aspose.words.fonts/fontfallbacksettings/
---
## FontFallbackSettings class

Gibt die Einstellungen für den Fallback-Mechanismus für Schriftarten an.

```csharp
public class FontFallbackSettings
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| [BuildAutomatic](../../aspose.words.fonts/fontfallbacksettings/buildautomatic/)() | Erstellt automatisch die Fallback-Einstellungen durch Scannen verfügbarer Schriftarten. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load)(Stream) | Lädt Fallback-Einstellungen aus dem XML-Stream. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load_1)(string) | Lädt Font-Fallback-Einstellungen aus der XML-Datei. |
| [LoadMsOfficeFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/)() | Lädt vordefinierte Fallback-Einstellungen, die das Fallback von Microsoft Word nachahmen und Microsoft Office-Schriftarten verwenden. |
| [LoadNotoFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/)() | Lädt vordefinierte Fallback-Einstellungen, die Google Noto-Schriftarten verwenden. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save)(Stream) | Speichert die aktuellen Fallback-Einstellungen im Stream. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save_1)(string) | Speichert die aktuellen Fallback-Einstellungen in einer Datei. |

### Bemerkungen

Standardmäßig werden Fallback-Einstellungen mit vordefinierten Einstellungen initialisiert, die das Fallback von Microsoft Word nachahmen.

### Beispiele

Zeigt, wie Fallback-Schriftarten über Unicode-Zeichencodebereiche verteilt werden.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Konfigurieren Sie unsere Schriftarteinstellungen so, dass Schriftarten nur aus dem Ordner „MyFonts“ stammen.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Der Aufruf der Methode "BuildAutomatic" generiert ein Fallback-Schema, das
// verteilt zugängliche Schriftarten auf so viele Unicode-Zeichencodes wie möglich.
// In unserem Fall hat es nur Zugriff auf eine Handvoll Schriftarten im Ordner "MyFonts".
fontFallbackSettings.BuildAutomatic();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// Wir können auch ein benutzerdefiniertes Substitutionsschema aus einer solchen Datei laden.
// Dieses Schema wendet die Schriftart "AllegroOpen" auf die Unicode-Blöcke "0000-00ff" an, die Schriftart "AllegroOpen" auf "0100-024f",
// und die Schriftart "M+ 2m" in allen anderen Bereichen, die andere Schriftarten im Schema nicht abdecken.
fontFallbackSettings.Load(MyDir + "Custom font fallback settings.xml");

// Erstellen Sie einen Document Builder und setzen Sie seine Schriftart auf eine Schriftart, die in keiner unserer Quellen vorhanden ist.
// Unsere Schriftarteinstellungen rufen das Fallback-Schema für Zeichen auf, die wir mit der nicht verfügbaren Schriftart eingeben.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Missing Font";

// Verwenden Sie den Builder, um jedes Unicode-Zeichen von 0x0021 bis 0x052F zu drucken,
// mit beschreibenden Linien, die Unicode-Blöcke teilen, die wir in unserem Fallback-Schema für benutzerdefinierte Schriftarten definiert haben.
for (int i = 0x0021; i < 0x0530; i++)
{
    switch (i)
    {
        case 0x0021:
            builder.Writeln(
                "\n\n0x0021 - 0x00FF: \nBasic Latin/Latin-1 Supplement Unicode blocks in \"AllegroOpen\" font:");
            break;
        case 0x0100:
            builder.Writeln(
                "\n\n0x0100 - 0x024F: \nLatin Extended A/B blocks, mostly in \"AllegroOpen\" font:");
            break;
        case 0x0250:
            builder.Writeln("\n\n0x0250 - 0x052F: \nIPA/Greek/Cyrillic blocks in \"M+ 2m\" font:");
            break;
    }

    builder.Write($"{Convert.ToChar(i)}");
}

doc.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.pdf");
```

### Siehe auch

* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)


