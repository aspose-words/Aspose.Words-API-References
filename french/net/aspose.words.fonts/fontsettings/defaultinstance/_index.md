---
title: FontSettings.DefaultInstance
linktitle: DefaultInstance
articleTitle: DefaultInstance
second_title: Aspose.Words pour .NET
description: FontSettings DefaultInstance propriété. Paramètres de police statiques par défaut en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.fonts/fontsettings/defaultinstance/
---
## FontSettings.DefaultInstance property

Paramètres de police statiques par défaut.

```csharp
public static FontSettings DefaultInstance { get; }
```

## Remarques

Cette instance est utilisée par défaut dans un document sauf si[`FontSettings`](../../../aspose.words/document/fontsettings/) est spécifié.

## Exemples

Montre comment configurer l’instance des paramètres de police par défaut.

```csharp
// Configurez l'instance des paramètres de police par défaut pour utiliser la police "Courier New"
// comme substitut de sauvegarde lorsque nous essayons d'utiliser une police inconnue.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.Enabled);

Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

// Ce document n'a pas de configuration FontSettings. Lorsque nous rendons le document,
// l'instance FontSettings par défaut résoudra la police manquante.
// Aspose.Words utilisera "Courier New" pour afficher le texte utilisant la police inconnue.
Assert.Null(doc.FontSettings);

doc.Save(ArtifactsDir + "FontSettings.DefaultFontInstance.pdf");
```

Montre comment utiliser l’interface IWarningCallback pour surveiller les avertissements de substitution de police.

```csharp
public void SubstitutionWarning()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Times New Roman";
    builder.Writeln("Hello world!");

    FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
    doc.WarningCallback = callback;

    // Stocke la collection actuelle de sources de polices, qui sera la source de polices par défaut pour chaque document
    // pour lequel nous ne spécifions pas de source de police différente.
    FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

    // À des fins de test, nous configurerons Aspose.Words pour qu'il recherche les polices uniquement dans un dossier qui n'existe pas.
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    // Lors du rendu du document, il n'y aura aucun endroit pour trouver la police "Times New Roman".
    // Cela provoquera un avertissement de substitution de police, que notre rappel détectera.
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

    Assert.True(callback.FontSubstitutionWarnings[0].WarningType == WarningType.FontSubstitution);
    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Equals(
            "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font.", StringComparison.Ordinal));
}

private class FontSubstitutionWarningCollector : IWarningCallback
{
    /// <summary>
    /// Appelé à chaque fois qu'un avertissement se produit lors du chargement/sauvegarde.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontSubstitutionWarnings.Warning(info);
    }

    public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

### Voir également

* class [FontSettings](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
