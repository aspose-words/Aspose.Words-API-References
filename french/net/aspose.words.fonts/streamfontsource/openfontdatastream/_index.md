---
title: StreamFontSource.OpenFontDataStream
linktitle: OpenFontDataStream
articleTitle: OpenFontDataStream
second_title: Aspose.Words pour .NET
description: StreamFontSource OpenFontDataStream méthode. Cette méthode devrait ouvrir le flux avec les données de police à la demande en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.fonts/streamfontsource/openfontdatastream/
---
## StreamFontSource.OpenFontDataStream method

Cette méthode devrait ouvrir le flux avec les données de police à la demande.

```csharp
public abstract Stream OpenFontDataStream()
```

### Return_Value

Flux de données de police.

## Remarques

Le flux sera fermé après la lecture. Il n'est pas nécessaire de le fermer explicitement.

## Exemples

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

* class [StreamFontSource](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
