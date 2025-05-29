---
title: EmbeddedFontStyle Enum
linktitle: EmbeddedFontStyle
articleTitle: EmbeddedFontStyle
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words EmbeddedFontStyle pour gérer facilement les styles de police intégrés dans les objets FontInfo, améliorant ainsi vos capacités de formatage de documents.
type: docs
weight: 3270
url: /fr/net/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enumeration

Spécifie le style d'une police incorporée à l'intérieur d'un[`FontInfo`](../fontinfo/) objet.

```csharp
[Flags]
public enum EmbeddedFontStyle
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Regular | `0` | Spécifie la police intégrée régulière. |
| Bold | `1` | Spécifie la police incorporée en gras. |
| Italic | `2` | Spécifie la police italique intégrée. |
| BoldItalic | `3` | Spécifie la police intégrée en gras-italique. |

## Exemples

Montre comment extraire une police intégrée d'un document et l'enregistrer sur le système de fichiers local.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Les formats de police intégrés peuvent être différents dans d'autres formats tels que .doc.
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
