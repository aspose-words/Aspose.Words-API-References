---
title: WarningInfoCollection Class
linktitle: WarningInfoCollection
articleTitle: WarningInfoCollection
second_title: Aspose.Words pour .NET
description: Découvrez Aspose.Words.WarningInfoCollection, une classe puissante pour gérer les objets WarningInfo, améliorant le traitement des documents et la gestion des erreurs.
type: docs
weight: 7490
url: /fr/net/aspose.words/warninginfocollection/
---
## WarningInfoCollection class

Représente une collection typée de[`WarningInfo`](../warninginfo/) objets.

Pour en savoir plus, visitez le[Programmation avec des documents](https://docs.aspose.com/words/net/programming-with-documents/) article de documentation.

```csharp
public class WarningInfoCollection : IEnumerable<WarningInfo>, IWarningCallback
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [WarningInfoCollection](warninginfocollection/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/warninginfocollection/count/) { get; } | Obtient le nombre d'éléments contenus dans la collection. |
| [Item](../../aspose.words/warninginfocollection/item/) { get; } | Obtient un élément à l'index spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Clear](../../aspose.words/warninginfocollection/clear/)() | Supprime tous les éléments de la collection. |
| [GetEnumerator](../../aspose.words/warninginfocollection/getenumerator/)() | Renvoie un objet énumérateur qui peut être utilisé pour parcourir tous les éléments de la collection. |
| [Warning](../../aspose.words/warninginfocollection/warning/)(*[WarningInfo](../warninginfo/)*) | Implémente le[`IWarningCallback`](../iwarningcallback/) interface. Ajoute un avertissement à cette collection. |

## Remarques

Vous pouvez utiliser cet objet de collection comme la forme la plus simple de[`IWarningCallback`](../iwarningcallback/) Implémentation pour collecter tous les avertissements générés par Aspose.Words lors d'une opération de chargement ou de sauvegarde. Créez une instance de cette classe et assignez-la à la classe[`WarningCallback`](../../aspose.words.loading/loadoptions/warningcallback/) ou[`WarningCallback`](../documentbase/warningcallback/) propriété.

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

* class [WarningInfo](../warninginfo/)
* interface [IWarningCallback](../iwarningcallback/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
