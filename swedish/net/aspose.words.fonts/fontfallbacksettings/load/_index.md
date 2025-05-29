---
title: FontFallbackSettings.Load
linktitle: Load
articleTitle: Load
second_title: Aspose.Words för .NET
description: Ladda och hantera enkelt alternativa teckensnittsinställningar från XML-filer med FontFallbackSettings Load-metoden för sömlös typografisk integration.
type: docs
weight: 20
url: /sv/net/aspose.words.fonts/fontfallbacksettings/load/
---
## Load(*string*) {#load_1}

Laddar alternativa teckensnittsinställningar från XML-filen.

```csharp
public void Load(string fileName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Inmatningsfilnamn. |

## Exempel

Visar hur man laddar och sparar alternativa teckensnittsinställningar till/från ett XML-dokument i det lokala filsystemet.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Laddar ett XML-dokument som definierar en uppsättning alternativa teckensnittsinställningar.
FontSettings fontSettings = new FontSettings();
fontSettings.FallbackSettings.Load(MyDir + "Font fallback rules.xml");

doc.FontSettings = fontSettings;
doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// Spara vårt dokuments nuvarande inställningar för teckensnittsreserv som ett XML-dokument.
doc.FontSettings.FallbackSettings.Save(ArtifactsDir + "FallbackSettings.xml");
```

### Se även

* class [FontFallbackSettings](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)

---

## Load(*Stream*) {#load}

Läser in reservinställningar från XML-strömmen.

```csharp
public void Load(Stream stream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Ingångsström. |

## Exempel

Visar hur man laddar och sparar alternativa teckensnittsinställningar till/från en ström.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Laddar ett XML-dokument som definierar en uppsättning alternativa teckensnittsinställningar.
using (FileStream fontFallbackStream = new FileStream(MyDir + "Font fallback rules.xml", FileMode.Open))
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.FallbackSettings.Load(fontFallbackStream);

    doc.FontSettings = fontSettings;
}

doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// Använd en ström för att spara vårt dokuments nuvarande teckensnittsinställningar som ett XML-dokument.
using (FileStream fontFallbackStream =
    new FileStream(ArtifactsDir + "FallbackSettings.xml", FileMode.Create))
{
    doc.FontSettings.FallbackSettings.Save(fontFallbackStream);
}
```

### Se även

* class [FontFallbackSettings](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
