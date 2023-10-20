---
title: FontFallbackSettings.Load
linktitle: Load
articleTitle: Load
second_title: Aspose.Words pour .NET
description: FontFallbackSettings Load méthode. Charge les paramètres de secours des polices à partir du fichier XML en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.fonts/fontfallbacksettings/load/
---
## Load(*string*) {#load_1}

Charge les paramètres de secours des polices à partir du fichier XML.

```csharp
public void Load(string fileName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Nom du fichier d'entrée. |

## Exemples

Montre comment charger et enregistrer les paramètres de secours des polices vers/depuis un document XML dans le système de fichiers local.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Charge un document XML qui définit un ensemble de paramètres de secours de police.
FontSettings fontSettings = new FontSettings();
fontSettings.FallbackSettings.Load(MyDir + "Font fallback rules.xml");

doc.FontSettings = fontSettings;
doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// Enregistrez les paramètres de secours de police actuels de notre document en tant que document XML.
doc.FontSettings.FallbackSettings.Save(ArtifactsDir + "FallbackSettings.xml");
```

### Voir également

* class [FontFallbackSettings](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)

---

## Load(*Stream*) {#load}

Charge les paramètres de secours à partir du flux XML.

```csharp
public void Load(Stream stream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Flux d'entrée. |

## Exemples

Montre comment charger et enregistrer les paramètres de secours des polices vers/depuis un flux.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Charge un document XML qui définit un ensemble de paramètres de secours de police.
using (FileStream fontFallbackStream = new FileStream(MyDir + "Font fallback rules.xml", FileMode.Open))
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.FallbackSettings.Load(fontFallbackStream);

    doc.FontSettings = fontSettings;
}

doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// Utiliser un flux pour enregistrer les paramètres de secours de police actuels de notre document en tant que document XML.
using (FileStream fontFallbackStream =
    new FileStream(ArtifactsDir + "FallbackSettings.xml", FileMode.Create))
{
    doc.FontSettings.FallbackSettings.Save(fontFallbackStream);
}
```

### Voir également

* class [FontFallbackSettings](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
