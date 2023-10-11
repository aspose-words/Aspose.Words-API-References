---
title: Enum EmbeddedFontStyle
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Fonts.EmbeddedFontStyle énumération. Spécifie le style dune police incorporée dans unFontInfo objet.
type: docs
weight: 2860
url: /fr/net/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enumeration

Spécifie le style d'une police incorporée dans un[`FontInfo`](../fontinfo/) objet.

```csharp
[Flags]
public enum EmbeddedFontStyle
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Regular | `0` | Spécifie la police intégrée régulière. |
| Bold | `1` | Spécifie la police intégrée grasse. |
| Italic | `2` | Spécifie la police italique intégrée. |
| BoldItalic | `3` | Spécifie la police intégrée gras-italique. |

### Exemples

Montre comment extraire une police incorporée d’un document et l’enregistrer dans le système de fichiers local.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Les formats de polices intégrées peuvent être différents dans d'autres formats tels que .doc.
// Nous devons connaître le format correct avant de pouvoir extraire la police.
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// Nous pouvons également convertir le format OpenType intégré, qui provient des documents .doc, en OpenType.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### Voir également

* espace de noms [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../)


