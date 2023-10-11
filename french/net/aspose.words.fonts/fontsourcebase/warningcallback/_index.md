---
title: FontSourceBase.WarningCallback
second_title: Référence de l'API Aspose.Words pour .NET
description: FontSourceBase propriété. Appelé lors du traitement de la source de police lorsquun problème susceptible dentraîner une perte de fidélité du formatage est détecté.
type: docs
weight: 30
url: /fr/net/aspose.words.fonts/fontsourcebase/warningcallback/
---
## FontSourceBase.WarningCallback property

Appelé lors du traitement de la source de police lorsqu'un problème susceptible d'entraîner une perte de fidélité du formatage est détecté.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

### Exemples

Montre comment appeler un rappel d'avertissement lorsque les sources de polices fonctionnent.

```csharp
public void FontSourceWarning()
{
    FontSettings settings = new FontSettings();
    settings.SetFontsFolder("bad folder?", false);

    FontSourceBase source = settings.GetFontsSources()[0];
    FontSourceWarningCollector callback = new FontSourceWarningCollector();
    source.WarningCallback = callback;

    // Récupère la liste des polices à appeler en rappel d'avertissement.
    IList<PhysicalFontInfo> fontInfos = source.GetAvailableFonts();

    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Contains("Error loading font from the folder \"bad folder?\""));
}

private class FontSourceWarningCollector : IWarningCallback
{
    /// <summary>
    /// Appelé chaque fois qu'un avertissement se produit lors du traitement de la source de police.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        FontSubstitutionWarnings.Warning(info);
    }

    public readonly WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

### Voir également

* interface [IWarningCallback](../../../aspose.words/iwarningcallback/)
* class [FontSourceBase](../)
* espace de noms [Aspose.Words.Fonts](../../fontsourcebase/)
* Assemblée [Aspose.Words](../../../)


