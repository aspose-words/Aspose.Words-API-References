---
title: FontFallbackSettings.Load
linktitle: Load
articleTitle: Load
second_title: Aspose.Words per .NET
description: Carica e gestisci senza sforzo le impostazioni di fallback dei font dai file XML con il metodo FontFallbackSettings Load per un'integrazione tipografica perfetta.
type: docs
weight: 20
url: /it/net/aspose.words.fonts/fontfallbacksettings/load/
---
## Load(*string*) {#load_1}

Carica le impostazioni di fallback del font dal file XML.

```csharp
public void Load(string fileName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Nome del file di input. |

## Esempi

Mostra come caricare e salvare le impostazioni di fallback dei font da/verso un documento XML nel file system locale.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Carica un documento XML che definisce un set di impostazioni di fallback dei font.
FontSettings fontSettings = new FontSettings();
fontSettings.FallbackSettings.Load(MyDir + "Font fallback rules.xml");

doc.FontSettings = fontSettings;
doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// Salva le impostazioni di fallback dei font correnti del nostro documento come documento XML.
doc.FontSettings.FallbackSettings.Save(ArtifactsDir + "FallbackSettings.xml");
```

### Guarda anche

* class [FontFallbackSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)

---

## Load(*Stream*) {#load}

Carica le impostazioni di fallback dal flusso XML.

```csharp
public void Load(Stream stream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Flusso di input. |

## Esempi

Mostra come caricare e salvare le impostazioni di fallback dei font da/verso un flusso.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Carica un documento XML che definisce un set di impostazioni di fallback dei font.
using (FileStream fontFallbackStream = new FileStream(MyDir + "Font fallback rules.xml", FileMode.Open))
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.FallbackSettings.Load(fontFallbackStream);

    doc.FontSettings = fontSettings;
}

doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// Utilizziamo un flusso per salvare le impostazioni di fallback dei font correnti del nostro documento come documento XML.
using (FileStream fontFallbackStream =
    new FileStream(ArtifactsDir + "FallbackSettings.xml", FileMode.Create))
{
    doc.FontSettings.FallbackSettings.Save(fontFallbackStream);
}
```

### Guarda anche

* class [FontFallbackSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
