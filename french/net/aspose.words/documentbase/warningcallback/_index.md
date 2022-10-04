---
title: WarningCallback
second_title: Référence de l'API Aspose.Words pour .NET
description: Appelé lors de diverses procédures de traitement de documents lorsquun problème est détecté pouvant entraîner une perte de fidélité des données ou du formatage.
type: docs
weight: 90
url: /fr/net/aspose.words/documentbase/warningcallback/
---
## DocumentBase.WarningCallback property

Appelé lors de diverses procédures de traitement de documents lorsqu'un problème est détecté pouvant entraîner une perte de fidélité des données ou du formatage.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

### Remarques

Le document peut générer des avertissements à n'importe quel stade de son existence, il est donc important de configurer le rappel d'avertissement le plus tôt possible pour éviter la perte d'avertissements. Par exemple, des propriétés telles que[`PageCount`](../../document/pagecount/) construit en fait la mise en page du document qui sera utilisée plus tard pour le rendu, et les avertissements de mise en page peuvent être perdus si le rappel d'avertissement est spécifié uniquement pour les appels de rendu ultérieurs.

### Exemples

Montre comment utiliser l'interface IWarningCallback pour surveiller les avertissements de substitution de polices.

```csharp
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

    // À des fins de test, nous allons définir Aspose.Words pour rechercher les polices uniquement dans un dossier qui n'existe pas.
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    // Lors du rendu du document, il n'y aura pas de place pour trouver la police "Times New Roman".
    // Cela provoquera un avertissement de substitution de police, que notre rappel détectera.
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Equals(
            "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
}

private class FontSubstitutionWarningCollector : IWarningCallback
{
    /// <summary>
    /// Appelé chaque fois qu'un avertissement se produit lors du chargement/sauvegarde.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontSubstitutionWarnings.Warning(info);
    }

    public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

Montre comment définir la propriété pour rechercher la correspondance la plus proche pour une police manquante à partir des sources de polices disponibles.

```csharp
[Test]
public void EnableFontSubstitution()
{
    // Ouvre un document contenant du texte formaté avec une police qui n'existe dans aucune de nos sources de polices.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Affecte un rappel pour gérer les avertissements de substitution de police.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Définir un nom de police par défaut et activer la substitution de police.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Nous recevrons un avertissement de substitution de police si nous enregistrons un document avec une police manquante.
    doc.FontSettings = fontSettings;
    doc.Save(ArtifactsDir + "FontSettings.EnableFontSubstitution.pdf");

    using (IEnumerator<WarningInfo> warnings = substitutionWarningHandler.FontWarnings.GetEnumerator())
        while (warnings.MoveNext())
            Console.WriteLine(warnings.Current.Description);

    // Nous pouvons également vérifier les avertissements dans la collection et les effacer.
    Assert.AreEqual(WarningSource.Layout, substitutionWarningHandler.FontWarnings[0].Source);
    Assert.AreEqual(
        "Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
        substitutionWarningHandler.FontWarnings[0].Description);

    substitutionWarningHandler.FontWarnings.Clear();

    Assert.That(substitutionWarningHandler.FontWarnings, Is.Empty);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// Appelé chaque fois qu'un avertissement se produit lors du chargement/sauvegarde.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontWarnings.Warning(info);
    }

    public WarningInfoCollection FontWarnings = new WarningInfoCollection();
}
```

### Voir également

* interface [IWarningCallback](../../iwarningcallback/)
* class [DocumentBase](../)
* espace de noms [Aspose.Words](../../documentbase/)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
