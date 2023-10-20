---
title: FileFontSource Class
linktitle: FileFontSource
articleTitle: FileFontSource
second_title: Aspose.Words pour .NET
description: Aspose.Words.Fonts.FileFontSource classe. Représente le fichier de police TrueType unique stocké dans le système de fichiers en C#.
type: docs
weight: 2870
url: /fr/net/aspose.words.fonts/filefontsource/
---
## FileFontSource class

Représente le fichier de police TrueType unique stocké dans le système de fichiers.

Pour en savoir plus, visitez le[Travailler avec des polices](https://docs.aspose.com/words/net/working-with-fonts/) article documentaire.

```csharp
public class FileFontSource : FontSourceBase
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FileFontSource](filefontsource/#constructor)(*string*) | Directeur. |
| [FileFontSource](filefontsource/#constructor_1)(*string, int*) | Directeur. |
| [FileFontSource](filefontsource/#constructor_2)(*string, int, string*) | Directeur. |

## Propriétés

| Nom | La description |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/filefontsource/cachekey/) { get; } | La clé de cette source dans le cache. |
| [FilePath](../../aspose.words.fonts/filefontsource/filepath/) { get; } | Chemin d'accès au fichier de police. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Renvoie la priorité de la source de police. |
| override [Type](../../aspose.words.fonts/filefontsource/type/) { get; } | Renvoie le type de la source de police. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Appelé lors du traitement de la source de police lorsqu'un problème susceptible d'entraîner une perte de fidélité du formatage est détecté. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Renvoie la liste des polices disponibles via cette source. |

## Exemples

Montre comment utiliser un fichier de police dans le système de fichiers local comme source de police.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### Voir également

* class [FontSourceBase](../fontsourcebase/)
* espace de noms [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../)
