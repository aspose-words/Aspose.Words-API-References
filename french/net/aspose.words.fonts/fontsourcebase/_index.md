---
title: FontSourceBase Class
linktitle: FontSourceBase
articleTitle: FontSourceBase
second_title: Aspose.Words pour .NET
description: Découvrez Aspose.Words.Fonts.FontSourceBase, la classe abstraite essentielle pour définir diverses sources de polices dans vos applications. Améliorez la mise en forme de vos documents !
type: docs
weight: 3410
url: /fr/net/aspose.words.fonts/fontsourcebase/
---
## FontSourceBase class

Il s'agit d'une classe de base abstraite pour les classes qui permettent à l'utilisateur de spécifier diverses sources de polices.

Pour en savoir plus, visitez le[Travailler avec les polices](https://docs.aspose.com/words/net/working-with-fonts/) article de documentation.

```csharp
public abstract class FontSourceBase
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Renvoie la priorité de la source de la police. |
| abstract [Type](../../aspose.words.fonts/fontsourcebase/type/) { get; } | Renvoie le type de la source de la police. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Appelé pendant le traitement de la source de police lorsqu'un problème est détecté qui pourrait entraîner une perte de fidélité du formatage. |

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

* espace de noms [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../)
