---
title: FontFallbackSettings.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words för .NET
description: FontFallbackSettings Save metod. Sparar de aktuella reservinställningarna för att streama i C#.
type: docs
weight: 50
url: /sv/net/aspose.words.fonts/fontfallbacksettings/save/
---
## Save(*Stream*) {#save}

Sparar de aktuella reservinställningarna för att streama.

```csharp
public void Save(Stream outputStream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| outputStream | Stream | Utgångsström. |

## Exempel

Visar hur man läser in och sparar reservinställningar för teckensnitt till/från en stream.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Ladda ett XML-dokument som definierar en uppsättning alternativa teckensnittsinställningar.
using (FileStream fontFallbackStream = new FileStream(MyDir + "Font fallback rules.xml", FileMode.Open))
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.FallbackSettings.Load(fontFallbackStream);

    doc.FontSettings = fontSettings;
}

doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// Använd en ström för att spara vårt dokuments aktuella typsnittsinställningar som ett XML-dokument.
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

Sparar de aktuella reservinställningarna i filen.

```csharp
public void Save(string fileName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Utdatafilnamn. |

## Exempel

Visar hur man läser in och sparar typsnittsalternativ till/från ett XML-dokument i det lokala filsystemet.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Ladda ett XML-dokument som definierar en uppsättning alternativa teckensnittsinställningar.
FontSettings fontSettings = new FontSettings();
fontSettings.FallbackSettings.Load(MyDir + "Font fallback rules.xml");

doc.FontSettings = fontSettings;
doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// Spara vårt dokuments nuvarande reservinställningar för typsnitt som ett XML-dokument.
doc.FontSettings.FallbackSettings.Save(ArtifactsDir + "FallbackSettings.xml");
```

### Se även

* class [FontFallbackSettings](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
