---
title: WarningType Enum
linktitle: WarningType
articleTitle: WarningType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.WarningType, qui catégorise les avertissements lors du chargement ou de l'enregistrement de documents, améliorant ainsi votre expérience de gestion de documents.
type: docs
weight: 7510
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
| DataLossCategory | `FF` | Certains textes/caractères/images ou autres données seront manquants soit dans l'arborescence du document après le chargement, soit dans le document créé après l'enregistrement. |
| DataLoss | `1` | Perte de données générique, pas de code spécifique. |
| MajorFormattingLossCategory | `FF00` | Le document résultant ou un emplacement particulier de celui-ci peut sembler sensiblement différent du document d'origine. |
| MajorFormattingLoss | `100` | Perte de formatage majeure générique, pas de code spécifique. |
| MinorFormattingLossCategory | `FF0000` | Le document résultant ou un emplacement particulier de celui-ci peut sembler quelque peu différent du document d'origine. |
| MinorFormattingLoss | `10000` | Perte de formatage mineure générique, pas de code spécifique. |
| FontSubstitution | `20000` | La police a été remplacée. |
| FontEmbedding | `40000` | Perte des informations de police intégrées lors de l'enregistrement du document. |
| UnexpectedContentCategory | `F000000` | Certains contenus du document source n'ont pas pu être reconnus (c'est-à-dire qu'ils ne sont pas pris en charge), cela peut ou non causer des problèmes ou entraîner une perte de données/formatage. |
| UnexpectedContent | `1000000` | Contenu générique inattendu, pas de code spécifique. |
| Hint | `10000000` | Signale un problème potentiel ou suggère une amélioration. |

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

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
