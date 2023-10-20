---
title: FontSettings.FallbackSettings
linktitle: FallbackSettings
articleTitle: FallbackSettings
second_title: Aspose.Words für .NET
description: FontSettings FallbackSettings eigendom. Einstellungen im Zusammenhang mit dem SchriftartFallbackMechanismus in C#.
type: docs
weight: 30
url: /de/net/aspose.words.fonts/fontsettings/fallbacksettings/
---
## FontSettings.FallbackSettings property

Einstellungen im Zusammenhang mit dem Schriftart-Fallback-Mechanismus.

```csharp
public FontFallbackSettings FallbackSettings { get; }
```

## Beispiele

Zeigt, wie Fallback-Schriftarten über Unicode-Zeichencodebereiche verteilt werden.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Konfigurieren Sie unsere Schriftarteinstellungen so, dass Schriftarten nur aus dem Ordner „MyFonts“ stammen.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Durch Aufrufen der Methode „BuildAutomatic“ wird ein Fallback-Schema generiert
// verteilt zugängliche Schriftarten auf möglichst viele Unicode-Zeichencodes.
// In unserem Fall hat es nur Zugriff auf die wenigen Schriftarten im Ordner „MyFonts“.
fontFallbackSettings.BuildAutomatic();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// Wir können auch ein benutzerdefiniertes Ersetzungsschema aus einer Datei wie dieser laden.
// Dieses Schema wendet die Schriftart „AllegroOpen“ auf die Unicode-Blöcke „0000-00ff“ und die Schriftart „AllegroOpen“ auf die Unicode-Blöcke „0100-024f“ an.
// und die Schriftart „M+ 2m“ in allen anderen Bereichen, die andere Schriftarten im Schema nicht abdecken.
fontFallbackSettings.Load(MyDir + "Custom font fallback settings.xml");

// Erstellen Sie einen Dokument-Builder und legen Sie seine Schriftart auf eine fest, die in keiner unserer Quellen vorhanden ist.
// Unsere Schriftarteinstellungen rufen das Fallback-Schema für Zeichen auf, die wir mit der nicht verfügbaren Schriftart eingeben.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Missing Font";

// Verwenden Sie den Builder, um jedes Unicode-Zeichen von 0x0021 bis 0x052F zu drucken.
// mit beschreibenden Zeilen, die Unicode-Blöcke unterteilen, die wir in unserem benutzerdefinierten Schriftart-Fallback-Schema definiert haben.
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

* class [FontFallbackSettings](../../fontfallbacksettings/)
* class [FontSettings](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
