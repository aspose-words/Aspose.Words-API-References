---
title: FontInfo.GetEmbeddedFontAsOpenType
linktitle: GetEmbeddedFontAsOpenType
articleTitle: GetEmbeddedFontAsOpenType
second_title: Aspose.Words pour .NET
description: FontInfo GetEmbeddedFontAsOpenType méthode. Obtient un fichier de police incorporé au format OpenType. Les polices au format Embedded OpenType sont converties en OpenType en C#.
type: docs
weight: 90
url: /fr/net/aspose.words.fonts/fontinfo/getembeddedfontasopentype/
---
## FontInfo.GetEmbeddedFontAsOpenType method

Obtient un fichier de police incorporé au format OpenType. Les polices au format Embedded OpenType sont converties en OpenType.

```csharp
public byte[] GetEmbeddedFontAsOpenType(EmbeddedFontStyle style)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| style | EmbeddedFontStyle | Spécifie le style de police à récupérer. |

### Return_Value

Retour`nul`si la police spécifiée n'est pas intégrée.

## Exemples

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

* enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* class [FontInfo](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
