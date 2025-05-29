---
title: FontFallbackSettings.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words för .NET
description: Spara enkelt dina FontFallback-inställningar med vår intuitiva sparmetod. Bevara dina anpassade reservinställningar för sömlös teckensnittshantering.
type: docs
weight: 50
url: /sv/net/aspose.words.fonts/fontfallbacksettings/save/
---
## Save(*Stream*) {#save}

Sparar de aktuella reservinställningarna för strömning.

```csharp
public void Save(Stream outputStream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| outputStream | Stream | Utgångsström. |

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

---

## Save(*string*) {#save_1}

Sparar de aktuella reservinställningarna till filen.

```csharp
public void Save(string fileName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Namn på utdatafil. |

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
