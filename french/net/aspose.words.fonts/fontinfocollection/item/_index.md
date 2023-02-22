---
title: FontInfoCollection.Item
second_title: Référence de l'API Aspose.Words pour .NET
description: FontInfoCollection propriété. Obtient une police avec le nom spécifié.
type: docs
weight: 40
url: /fr/net/aspose.words.fonts/fontinfocollection/item/
---
## FontInfoCollection indexer (1 of 2)

Obtient une police avec le nom spécifié.

```csharp
public FontInfo this[string name] { get; }
```

| Paramètre | La description |
| --- | --- |
| name | Nom insensible à la casse de la police à localiser. |

### Exemples

Montre comment extraire une police incorporée d'un document et l'enregistrer dans le système de fichiers local.

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

// De plus, nous pouvons convertir le format OpenType intégré, qui provient des documents .doc, en OpenType.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### Voir également

* class [FontInfo](../../fontinfo/)
* class [FontInfoCollection](../)
* espace de noms [Aspose.Words.Fonts](../../fontinfocollection/)
* Assemblée [Aspose.Words](../../../)

---

## FontInfoCollection indexer (2 of 2)

Obtient une police à l'index spécifié.

```csharp
public FontInfo this[int index] { get; }
```

| Paramètre | La description |
| --- | --- |
| index | Index de base zéro de la police. |

### Exemples

Montre comment extraire une police incorporée d'un document et l'enregistrer dans le système de fichiers local.

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

// De plus, nous pouvons convertir le format OpenType intégré, qui provient des documents .doc, en OpenType.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### Voir également

* class [FontInfo](../../fontinfo/)
* class [FontInfoCollection](../)
* espace de noms [Aspose.Words.Fonts](../../fontinfocollection/)
* Assemblée [Aspose.Words](../../../)


