---
title: MemoryFontSource Class
linktitle: MemoryFontSource
articleTitle: MemoryFontSource
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fonts.MemoryFontSource, permettant un accès transparent aux polices TrueType stockées en mémoire pour un traitement amélioré des documents.
type: docs
weight: 3450
url: /fr/net/aspose.words.fonts/memoryfontsource/
---
## MemoryFontSource class

Représente le fichier de police TrueType unique stocké en mémoire.

Pour en savoir plus, visitez le[Travailler avec les polices](https://docs.aspose.com/words/net/working-with-fonts/) article de documentation.

```csharp
public class MemoryFontSource : FontSourceBase
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [MemoryFontSource](memoryfontsource/#constructor)(*byte[]*) | Cteur. |
| [MemoryFontSource](memoryfontsource/#constructor_1)(*byte[], int*) | Cteur. |
| [MemoryFontSource](memoryfontsource/#constructor_2)(*byte[], int, string*) | Cteur. |

## Propriétés

| Nom | La description |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/memoryfontsource/cachekey/) { get; } | La clé de cette source dans le cache. |
| [FontData](../../aspose.words.fonts/memoryfontsource/fontdata/) { get; } | Données de police binaires. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Renvoie la priorité de la source de la police. |
| override [Type](../../aspose.words.fonts/memoryfontsource/type/) { get; } | Renvoie le type de la source de la police. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Appelé pendant le traitement de la source de police lorsqu'un problème est détecté qui pourrait entraîner une perte de fidélité du formatage. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Renvoie la liste des polices disponibles via cette source. |

## Exemples

Montre comment utiliser un tableau d'octets avec des données provenant d'un fichier de police comme source de police.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### Voir également

* class [FontSourceBase](../fontsourcebase/)
* espace de noms [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../)
