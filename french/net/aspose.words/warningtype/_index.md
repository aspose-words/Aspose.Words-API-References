---
title: Enum WarningType
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.WarningType énumération. Spécifie le type davertissement émis par Aspose.Words lors du chargement ou de lenregistrement du document.
type: docs
weight: 6660
url: /fr/net/aspose.words/warningtype/
---
## WarningType enumeration

Spécifie le type d'avertissement émis par Aspose.Words lors du chargement ou de l'enregistrement du document.

```csharp
[Flags]
public enum WarningType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| DataLossCategory | `FF` | Certains textes/caractères/images ou autres données seront manquants soit dans l'arborescence du document après le chargement, , soit dans le document créé après la sauvegarde. |
| DataLoss | `1` | Perte de données génériques, pas de code spécifique. |
| MajorFormattingLossCategory | `FF00` | Le document résultant ou un emplacement particulier de celui-ci peut être sensiblement différent par rapport au document original. |
| MajorFormattingLoss | `100` | Perte de formatage majeure générique, pas de code spécifique. |
| MinorFormattingLossCategory | `FF0000` | Le document résultant ou un emplacement particulier de celui-ci peut sembler quelque peu différent par rapport au document original. |
| MinorFormattingLoss | `10000` | Perte de formatage mineure générique, pas de code spécifique. |
| FontSubstitution | `20000` | La police a été remplacée. |
| FontEmbedding | `40000` | Perte des informations sur la police intégrée lors de l'enregistrement du document. |
| UnexpectedContentCategory | `F000000` | Certains contenus du document source n'ont pas pu être reconnus (c'est-à-dire qu'ils ne sont pas pris en charge), cela peut ou non provoquer des problèmes ou entraîner une perte de données/de formatage. |
| UnexpectedContent | `1000000` | Contenu générique inattendu, pas de code spécifique. |
| Hint | `10000000` | Informe d'un problème potentiel ou suggère une amélioration. |

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

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


