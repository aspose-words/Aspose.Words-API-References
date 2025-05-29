---
title: StreamFontSource Class
linktitle: StreamFontSource
articleTitle: StreamFontSource
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fonts.StreamFontSource, votre solution de référence pour les sources de polices de flux personnalisées qui améliorent la flexibilité et la conception des documents.
type: docs
weight: 3470
url: /fr/net/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class

Classe de base pour la source de police de flux définie par l'utilisateur.

Pour en savoir plus, visitez le[Travailler avec les polices](https://docs.aspose.com/words/net/working-with-fonts/) article de documentation.

```csharp
public abstract class StreamFontSource : FontSourceBase,   
```

## Propriétés

| Nom | La description |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/streamfontsource/cachekey/) { get; } | La clé de cette source dans le cache. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Renvoie la priorité de la source de la police. |
| [Type](../../aspose.words.fonts/streamfontsource/type/) { get; } | Renvoie le type de la source de la police. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Appelé pendant le traitement de la source de police lorsqu'un problème est détecté qui pourrait entraîner une perte de fidélité du formatage. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Renvoie la liste des polices disponibles via cette source. |
| abstract [OpenFontDataStream](../../aspose.words.fonts/streamfontsource/openfontdatastream/)() | Cette méthode devrait ouvrir le flux avec les données de police à la demande. |

## Remarques

Pour utiliser la source de police de flux, vous devez créer une classe dérivée à partir de la`StreamFontSource` et fournir la mise en œuvre du[`OpenFontDataStream`](./openfontdatastream/) méthode.

[`OpenFontDataStream`](./openfontdatastream/)La méthode peut être appelée plusieurs fois. Pour la première fois, elle sera appelée lorsqu'Aspose.Words analysera les sources de polices fournies pour obtenir la liste des polices disponibles. Elle pourra ensuite être appelée si la police est utilisée dans le document pour analyser les données de police et les intégrer à certains formats de sortie.

`StreamFontSource` peut être utile car cela permet de charger les données de police uniquement lorsque cela est nécessaire et de ne pas les stocker en mémoire pour le[`FontSettings`](../fontsettings/) durée de vie.

## Exemples

Montre comment charger des polices à partir du flux.

```csharp
public void StreamFontSourceFileRendering()
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.SetFontsSources(new FontSourceBase[] {new StreamFontSourceFile()});

    DocumentBuilder builder = new DocumentBuilder();
    builder.Document.FontSettings = fontSettings;
    builder.Font.Name = "Kreon-Regular";
    builder.Writeln("Test aspose text when saving to PDF.");

    builder.Document.Save(ArtifactsDir + "FontSettings.StreamFontSourceFileRendering.pdf");
}

/// <summary>
/// Chargez les données de police uniquement lorsque cela est nécessaire au lieu de les stocker dans la mémoire
/// pendant toute la durée de vie de l'objet « FontSettings ».
/// </summary>
private class StreamFontSourceFile : StreamFontSource
{
    public override Stream OpenFontDataStream()
    {
        return File.OpenRead(FontsDir + "Kreon-Regular.ttf");
    }
}
```

### Voir également

* class [FontSourceBase](../fontsourcebase/)
* interface [  ](../../global/%02  /)
* espace de noms [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../)
