---
title: Class StreamFontSource
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Fonts.StreamFontSource classe. Classe de base pour la source de police de flux définie par lutilisateur.
type: docs
weight: 3040
url: /fr/net/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class

Classe de base pour la source de police de flux définie par l'utilisateur.

Pour en savoir plus, visitez le[Travailler avec des polices](https://docs.aspose.com/words/net/working-with-fonts/) article documentaire.

```csharp
public abstract class StreamFontSource : FontSourceBase
```

## Propriétés

| Nom | La description |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/streamfontsource/cachekey/) { get; } | La clé de cette source dans le cache. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Renvoie la priorité de la source de police. |
| [Type](../../aspose.words.fonts/streamfontsource/type/) { get; } | Renvoie le type de la source de police. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Appelé lors du traitement de la source de police lorsqu'un problème susceptible d'entraîner une perte de fidélité du formatage est détecté. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Renvoie la liste des polices disponibles via cette source. |
| abstract [OpenFontDataStream](../../aspose.words.fonts/streamfontsource/openfontdatastream/)() | Cette méthode devrait ouvrir le flux avec les données de police à la demande. |

### Remarques

Afin d'utiliser la source de police de flux, vous devez créer une classe dérivée à partir du`StreamFontSource` et assurer la mise en œuvre du[`OpenFontDataStream`](./openfontdatastream/) méthode.

[`OpenFontDataStream`](./openfontdatastream/)La méthode peut être appelée plusieurs fois. Pour la première fois, il sera appelé lorsqu'Aspose.Words analysera les sources de polices fournies pour obtenir la liste des polices disponibles. Plus tard, il peut être appelé si la police est utilisée dans le document pour analyser les données de police et pour intégrer les données de police dans certains formats de sortie.

`StreamFontSource` peut être utile car cela permet de charger les données de police uniquement lorsqu'elles sont requises et de ne pas les stocker en mémoire pour le[`FontSettings`](../fontsettings/) durée de vie.

### Exemples

Montre comment charger les polices à partir du flux.

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
/// Charge les données de police uniquement lorsque cela est nécessaire au lieu de les stocker dans la mémoire
/// pendant toute la durée de vie de l'objet "FontSettings".
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
* espace de noms [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../)


