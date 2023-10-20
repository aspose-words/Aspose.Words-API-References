---
title: FontFallbackSettings.Load
linktitle: Load
articleTitle: Load
second_title: Aspose.Words per .NET
description: FontFallbackSettings Load metodo. Carica le impostazioni di fallback dei caratteri dal file XML in C#.
type: docs
weight: 20
url: /it/net/aspose.words.fonts/fontfallbacksettings/load/
---
## Load(*string*) {#load_1}

Carica le impostazioni di fallback dei caratteri dal file XML.

```csharp
public void Load(string fileName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Inserisci il nome del file. |

## Esempi

Mostra come caricare e salvare le impostazioni di fallback dei caratteri in/da un documento XML nel file system locale.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Carica un documento XML che definisce una serie di impostazioni di fallback dei caratteri.
FontSettings fontSettings = new FontSettings();
fontSettings.FallbackSettings.Load(MyDir + "Font fallback rules.xml");

doc.FontSettings = fontSettings;
doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// Salva le attuali impostazioni di fallback dei caratteri del nostro documento come documento XML.
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

Mostra come caricare e salvare le impostazioni di fallback dei caratteri in/da un flusso.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Carica un documento XML che definisce una serie di impostazioni di fallback dei caratteri.
using (FileStream fontFallbackStream = new FileStream(MyDir + "Font fallback rules.xml", FileMode.Open))
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.FallbackSettings.Load(fontFallbackStream);

    doc.FontSettings = fontSettings;
}

doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// Utilizza uno stream per salvare le impostazioni di fallback dei caratteri correnti del nostro documento come documento XML.
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
