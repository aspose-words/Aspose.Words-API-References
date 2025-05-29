---
title: FontFallbackSettings.Load
linktitle: Load
articleTitle: Load
second_title: Aspose.Words pour .NET
description: Chargez et gérez sans effort les paramètres de secours des polices à partir de fichiers XML avec la méthode de chargement FontFallbackSettings pour une intégration typographique transparente.
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

// Chargez un document XML qui définit un ensemble de paramètres de police de secours.
FontSettings fontSettings = new FontSettings();
fontSettings.FallbackSettings.Load(MyDir + "Font fallback rules.xml");

doc.FontSettings = fontSettings;
doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// Enregistrez les paramètres de police de secours actuels de notre document sous forme de document XML.
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

// Chargez un document XML qui définit un ensemble de paramètres de police de secours.
using (FileStream fontFallbackStream = new FileStream(MyDir + "Font fallback rules.xml", FileMode.Open))
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.FallbackSettings.Load(fontFallbackStream);

    doc.FontSettings = fontSettings;
}

doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// Utilisez un flux pour enregistrer les paramètres de police de secours actuels de notre document sous forme de document XML.
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
