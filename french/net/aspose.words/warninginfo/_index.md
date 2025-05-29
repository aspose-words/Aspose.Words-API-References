---
title: WarningInfo Class
linktitle: WarningInfo
articleTitle: WarningInfo
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.WarningInfo, qui fournit des informations cruciales sur les avertissements lors du chargement ou de l'enregistrement de documents, améliorant ainsi l'efficacité de votre flux de travail.
type: docs
weight: 7480
url: /fr/net/aspose.words/warninginfo/
---
## WarningInfo class

Contient des informations sur un avertissement émis par Aspose.Words lors du chargement ou de l'enregistrement du document.

Pour en savoir plus, visitez le[Programmation avec des documents](https://docs.aspose.com/words/net/programming-with-documents/) article de documentation.

```csharp
public class WarningInfo
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Description](../../aspose.words/warninginfo/description/) { get; } | Renvoie la description de l'avertissement. |
| [Source](../../aspose.words/warninginfo/source/) { get; } | Renvoie la source de l'avertissement. |
| [WarningType](../../aspose.words/warninginfo/warningtype/) { get; } | Renvoie le type de l'avertissement. |

## Remarques

Vous ne créez pas d'instances de cette classe. Les objets de cette classe sont created et transmis par Aspose.Words à[`Warning`](../iwarningcallback/warning/) méthode.

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
