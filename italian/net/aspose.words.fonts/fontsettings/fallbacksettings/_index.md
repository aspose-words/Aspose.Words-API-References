---
title: FontSettings.FallbackSettings
linktitle: FallbackSettings
articleTitle: FallbackSettings
second_title: Aspose.Words per .NET
description: Scopri la proprietà FontSettings FallbackSettings per meccanismi di fallback ottimizzati per i font. Migliora il tuo design con un rendering del testo impeccabile!
type: docs
weight: 30
url: /it/net/aspose.words.fonts/fontsettings/fallbacksettings/
---
## FontSettings.FallbackSettings property

Impostazioni relative al meccanismo di fallback dei font.

```csharp
public FontFallbackSettings FallbackSettings { get; }
```

## Esempi

Mostra come distribuire i font di fallback tra gli intervalli di codici di caratteri Unicode.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Configura le impostazioni dei font in modo che i font provengano solo dalla cartella "MyFonts".
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// La chiamata al metodo "BuildAutomatic" genererà uno schema di fallback che
// distribuisce i font accessibili nel maggior numero possibile di codici di caratteri Unicode.
// Nel nostro caso, ha accesso solo ai pochi font presenti nella cartella "MyFonts".
fontFallbackSettings.BuildAutomatic();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// Possiamo anche caricare uno schema di sostituzione personalizzato da un file come questo.
// Questo schema applica il font "AllegroOpen" sui blocchi Unicode "0000-00ff", il font "AllegroOpen" su "0100-024f",
// e il font "M+ 2m" in tutti gli altri intervalli non coperti dagli altri font nello schema.
fontFallbackSettings.Load(MyDir + "Custom font fallback settings.xml");

// Crea un generatore di documenti e imposta il font su uno che non esiste in nessuna delle nostre fonti.
// Le nostre impostazioni del font richiameranno lo schema di fallback per i caratteri che digitiamo utilizzando il font non disponibile.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Missing Font";

// Utilizzare il builder per stampare tutti i caratteri Unicode da 0x0021 a 0x052F,
// con linee descrittive che dividono i blocchi Unicode definiti nel nostro schema di fallback dei font personalizzato.
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

### Guarda anche

* class [FontFallbackSettings](../../fontfallbacksettings/)
* class [FontSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
