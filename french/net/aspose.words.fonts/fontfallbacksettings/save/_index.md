---
title: FontFallbackSettings.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words pour .NET
description: Enregistrez facilement vos paramètres FontFallbackSettings grâce à notre méthode d'enregistrement intuitive. Conservez vos paramètres de secours personnalisés pour une gestion fluide des polices.
type: docs
weight: 50
url: /fr/net/aspose.words.fonts/fontfallbacksettings/save/
---
## Save(*Stream*) {#save}

Enregistre les paramètres de secours actuels dans le flux.

```csharp
public void Save(Stream outputStream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| outputStream | Stream | Flux de sortie. |

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

---

## Save(*string*) {#save_1}

Enregistre les paramètres de secours actuels dans un fichier.

```csharp
public void Save(string fileName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Nom du fichier de sortie. |

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
