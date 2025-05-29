---
title: FontFallbackSettings.BuildAutomatic
linktitle: BuildAutomatic
articleTitle: BuildAutomatic
second_title: Aspose.Words für .NET
description: Entdecken Sie die BuildAutomatic-Methode „FontFallbackSettings“, die mühelos Schriftarten scannt, um optimale Fallback-Einstellungen für verbesserte Typografie zu erstellen.
type: docs
weight: 10
url: /de/net/aspose.words.fonts/fontfallbacksettings/buildautomatic/
---
## FontFallbackSettings.BuildAutomatic method

Erstellt automatisch die Fallback-Einstellungen durch Scannen verfügbarer Schriftarten.

```csharp
public void BuildAutomatic()
```

## Bemerkungen

Diese Methode kann zu nicht optimalen Fallback-Einstellungen führen. Schriftarten werden überprüft durch[ Unicode-Zeichenbereich](https://docs.microsoft.com/en-us/typography/opentype/spec/os2#ur) Felder und nicht durch das tatsächliche Vorhandensein von Glyphen. Auch Unicode-Bereiche werden einzeln geprüft und mehrere Bereiche, die sich auf eine einzelne Sprache/ein einzelnes Skript beziehen, können unterschiedliche Ersatzschriftarten verwenden.

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

* class [FontFallbackSettings](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
