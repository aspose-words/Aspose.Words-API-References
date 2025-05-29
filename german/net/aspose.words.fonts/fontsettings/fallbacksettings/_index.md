---
title: FontSettings.FallbackSettings
linktitle: FallbackSettings
articleTitle: FallbackSettings
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FontSettings FallbackSettings“ für optimierte Fallback-Mechanismen für Schriftarten. Verbessern Sie Ihr Design mit nahtloser Textdarstellung!
type: docs
weight: 30
url: /de/net/aspose.words.fonts/fontsettings/fallbacksettings/
---
## FontSettings.FallbackSettings property

Einstellungen im Zusammenhang mit dem Font-Fallback-Mechanismus.

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

// Konfigurieren Sie unsere Schriftarteinstellungen so, dass Schriftarten nur aus dem Ordner „MyFonts“ bezogen werden.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Durch Aufrufen der Methode „BuildAutomatic“ wird ein Fallback-Schema generiert, das
// verteilt zugängliche Schriftarten auf so viele Unicode-Zeichencodes wie möglich.
// In unserem Fall hat es nur Zugriff auf die Handvoll Schriftarten im Ordner „MyFonts“.
fontFallbackSettings.BuildAutomatic();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// Wir können auch ein benutzerdefiniertes Substitutionsschema aus einer Datei wie dieser laden.
// Dieses Schema wendet die Schriftart "AllegroOpen" auf die Unicode-Blöcke "0000-00ff" an, die Schriftart "AllegroOpen" auf die Blöcke "0100-024f",
// und die Schriftart „M+ 2m“ in allen anderen Bereichen, die von anderen Schriftarten im Schema nicht abgedeckt werden.
fontFallbackSettings.Load(MyDir + "Custom font fallback settings.xml");

// Erstellen Sie einen Dokumentgenerator und legen Sie seine Schriftart auf eine fest, die in keiner unserer Quellen vorhanden ist.
// Unsere Schriftarteinstellungen rufen das Fallback-Schema für Zeichen auf, die wir mit der nicht verfügbaren Schriftart eingeben.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Missing Font";

// Verwenden Sie den Builder, um jedes Unicode-Zeichen von 0x0021 bis 0x052F zu drucken.
// mit beschreibenden Linien, die die Unicode-Blöcke trennen, die wir in unserem benutzerdefinierten Schriftart-Fallback-Schema definiert haben.
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
