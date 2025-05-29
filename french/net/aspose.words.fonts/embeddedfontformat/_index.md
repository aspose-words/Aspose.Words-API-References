---
title: EmbeddedFontFormat Enum
linktitle: EmbeddedFontFormat
articleTitle: EmbeddedFontFormat
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.EmbeddedFontFormat, qui définit les formats des polices intégrées dans l'objet FontInfo pour un style de document amélioré.
type: docs
weight: 3260
url: /fr/net/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enumeration

Spécifie le format d'une police intégrée particulière à l'intérieur[`FontInfo`](../fontinfo/) objet.

Lors de l'enregistrement d'un document dans un fichier, seules les polices intégrées du format correspondant sont écrites.

```csharp
public enum EmbeddedFontFormat
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| EmbeddedOpenType | `0` | Spécifie le format de fichier Embedded OpenType (EOT). |
| OpenType | `1` | Spécifie la police, intégrée en tant que copie simple du fichier de police OpenType (TrueType). |

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
