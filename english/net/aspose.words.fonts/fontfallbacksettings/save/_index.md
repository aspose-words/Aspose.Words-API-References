---
title: FontFallbackSettings.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words for .NET
description: FontFallbackSettings Save method. Saves the current fallback settings to stream in C#.
type: docs
weight: 50
url: /net/aspose.words.fonts/fontfallbacksettings/save/
---
## Save(*Stream*) {#save}

Saves the current fallback settings to stream.

```csharp
public void Save(Stream outputStream)
```

| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | Stream | Output stream. |

## Examples

Shows how to load and save font fallback settings to/from a stream.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Load an XML document that defines a set of font fallback settings.
using (FileStream fontFallbackStream = new FileStream(MyDir + "Font fallback rules.xml", FileMode.Open))
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.FallbackSettings.Load(fontFallbackStream);

    doc.FontSettings = fontSettings;
}

doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// Use a stream to save our document's current font fallback settings as an XML document.
using (FileStream fontFallbackStream =
    new FileStream(ArtifactsDir + "FallbackSettings.xml", FileMode.Create))
{
    doc.FontSettings.FallbackSettings.Save(fontFallbackStream);
}
```

### See Also

* class [FontFallbackSettings](../)
* namespace [Aspose.Words.Fonts](../../fontfallbacksettings/)
* assembly [Aspose.Words](../../../)

---

## Save(*string*) {#save_1}

Saves the current fallback settings to file.

```csharp
public void Save(string fileName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | Output file name. |

## Examples

Shows how to load and save font fallback settings to/from an XML document in the local file system.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Load an XML document that defines a set of font fallback settings.
FontSettings fontSettings = new FontSettings();
fontSettings.FallbackSettings.Load(MyDir + "Font fallback rules.xml");

doc.FontSettings = fontSettings;
doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// Save our document's current font fallback settings as an XML document.
doc.FontSettings.FallbackSettings.Save(ArtifactsDir + "FallbackSettings.xml");
```

### See Also

* class [FontFallbackSettings](../)
* namespace [Aspose.Words.Fonts](../../fontfallbacksettings/)
* assembly [Aspose.Words](../../../)
