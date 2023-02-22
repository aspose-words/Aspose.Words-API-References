---
title: FontFallbackSettings.BuildAutomatic
second_title: Aspose.Words für .NET-API-Referenz
description: FontFallbackSettings methode. Erstellt automatisch die FallbackEinstellungen durch Scannen verfügbarer Schriftarten.
type: docs
weight: 10
url: /de/net/aspose.words.fonts/fontfallbacksettings/buildautomatic/
---
## FontFallbackSettings.BuildAutomatic method

Erstellt automatisch die Fallback-Einstellungen durch Scannen verfügbarer Schriftarten.

```csharp
public void BuildAutomatic()
```

### Bemerkungen

Diese Methode kann zu nicht optimalen Fallback-Einstellungen führen. Schriften werden von geprüft[ Unicode-Zeichenbereich](https://docs.microsoft.com/en-us/typography/opentype/spec/os2#ur) Felder und nicht durch das tatsächliche Vorhandensein von Glyphen. Auch Unicode-Bereiche werden einzeln überprüft und mehrere Bereiche, die sich auf eine einzelne Sprache/Skript beziehen, können unterschiedliche Fallback-Schriftarten verwenden.

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

* class [FontFallbackSettings](../)
* namensraum [Aspose.Words.Fonts](../../fontfallbacksettings/)
* Montage [Aspose.Words](../../../)


