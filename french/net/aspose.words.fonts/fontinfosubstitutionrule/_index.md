---
title: Class FontInfoSubstitutionRule
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Fonts.FontInfoSubstitutionRule classe. Règle de substitution des informations de police.
type: docs
weight: 2940
url: /fr/net/aspose.words.fonts/fontinfosubstitutionrule/
---
## FontInfoSubstitutionRule class

Règle de substitution des informations de police.

Pour en savoir plus, visitez le[Travailler avec des polices](https://docs.aspose.com/words/net/working-with-fonts/) article documentaire.

```csharp
public class FontInfoSubstitutionRule : FontSubstitutionRule
```

## Propriétés

| Nom | La description |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Spécifie si la règle est activée ou non. |

### Remarques

Selon cette règle, Aspose.Words évalue tous les champs associés dans[`FontInfo`](../fontinfo/) (Panose, Sig, etc.) for la police manquante et trouve la correspondance la plus proche parmi les sources de polices disponibles. Si[`FontInfo`](../fontinfo/)n'est pas disponible pour la police manquante alors rien ne sera fait.

### Exemples

Montre comment définir la propriété permettant de trouver la correspondance la plus proche pour une police manquante à partir des sources de polices disponibles.

```csharp
public void EnableFontSubstitution()
{
    // Ouvre un document contenant du texte formaté avec une police qui n'existe dans aucune de nos sources de polices.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Attribue un rappel pour gérer les avertissements de substitution de police.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Définit un nom de police par défaut et active la substitution de police.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Les métriques de police d'origine doivent être utilisées après la substitution de police.
    doc.LayoutOptions.KeepOriginalFontMetrics = true;

    // Nous recevrons un avertissement de substitution de police si nous enregistrons un document avec une police manquante.
    doc.FontSettings = fontSettings;
    doc.Save(ArtifactsDir + "FontSettings.EnableFontSubstitution.pdf");

    using (IEnumerator<WarningInfo> warnings = substitutionWarningHandler.FontWarnings.GetEnumerator())
        while (warnings.MoveNext())
            Console.WriteLine(warnings.Current.Description);

    // Nous pouvons également vérifier les avertissements de la collection et les effacer.
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
    /// Appelé à chaque fois qu'un avertissement se produit lors du chargement/sauvegarde.
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

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* espace de noms [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../)


