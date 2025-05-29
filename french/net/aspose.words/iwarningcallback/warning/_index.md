---
title: IWarningCallback.Warning
linktitle: Warning
articleTitle: Warning
second_title: Aspose.Words pour .NET
description: Découvrez la méthode IWarningCallback dans Aspose.Words. Gérez facilement les problèmes de chargement et d'enregistrement de documents, en préservant la mise en forme et l'intégrité des données.
type: docs
weight: 10
url: /fr/net/aspose.words/iwarningcallback/warning/
---
## IWarningCallback.Warning method

Aspose.Words invoque cette méthode lorsqu'il rencontre un problème lors du chargement ou de l'enregistrement d'un document qui pourrait entraîner une perte de formatage ou de fidélité des données.

```csharp
public void Warning(WarningInfo info)
```

## Exemples

Montre comment définir la propriété permettant de trouver la correspondance la plus proche pour une police manquante parmi les sources de polices disponibles.

```csharp
public void EnableFontSubstitution()
{
    // Ouvrez un document contenant du texte formaté avec une police qui n'existe dans aucune de nos sources de polices.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Attribuer un rappel pour gérer les avertissements de substitution de police.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Définissez un nom de police par défaut et activez la substitution de police.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Les mesures de police d'origine doivent être utilisées après la substitution de police.
    doc.LayoutOptions.KeepOriginalFontMetrics = true;

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

    Assert.AreEqual(0, substitutionWarningHandler.FontWarnings.Count);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// Appelé chaque fois qu'un avertissement se produit pendant le chargement/la sauvegarde.
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

* class [WarningInfo](../../warninginfo/)
* interface [IWarningCallback](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
