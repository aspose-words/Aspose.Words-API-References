---
title: Class FontSourceBase
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Fonts.FontSourceBase classe. Il sagit dune classe de base abstraite pour les classes qui permettent à lutilisateur de spécifier diverses sources de polices.
type: docs
weight: 2800
url: /fr/net/aspose.words.fonts/fontsourcebase/
---
## FontSourceBase class

Il s'agit d'une classe de base abstraite pour les classes qui permettent à l'utilisateur de spécifier diverses sources de polices.

```csharp
public abstract class FontSourceBase
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Renvoie la priorité de la source de la police. |
| abstract [Type](../../aspose.words.fonts/fontsourcebase/type/) { get; } | Renvoie le type de la source de la police. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Appelé lors du traitement de la source de la police lorsqu'un problème est détecté pouvant entraîner une perte de fidélité de formatage. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Renvoie la liste des polices disponibles via cette source. |

### Exemples

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


