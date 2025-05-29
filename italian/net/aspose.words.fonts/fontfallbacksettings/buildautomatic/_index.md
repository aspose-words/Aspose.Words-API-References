---
title: FontFallbackSettings.BuildAutomatic
linktitle: BuildAutomatic
articleTitle: BuildAutomatic
second_title: Aspose.Words per .NET
description: Scopri il metodo FontFallbackSettings BuildAutomatic che analizza senza sforzo i font per creare impostazioni di fallback ottimali per una tipografia migliorata.
type: docs
weight: 10
url: /it/net/aspose.words.fonts/fontfallbacksettings/buildautomatic/
---
## FontFallbackSettings.BuildAutomatic method

Crea automaticamente le impostazioni di fallback eseguendo la scansione dei font disponibili.

```csharp
public void BuildAutomatic()
```

## Osservazioni

Questo metodo potrebbe produrre impostazioni di fallback non ottimali. I font vengono controllati da[ Intervallo di caratteri Unicode](https://docs.microsoft.com/en-us/typography/opentype/spec/os2#ur) campi e non dalla presenza effettiva dei glifi. Anche gli intervalli Unicode vengono controllati individualmente e diversi intervalli relativi a una singola lingua/alfabeto potrebbero utilizzare font di fallback diversi.

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

* class [FontFallbackSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
