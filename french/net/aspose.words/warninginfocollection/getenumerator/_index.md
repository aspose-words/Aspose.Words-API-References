---
title: WarningInfoCollection.GetEnumerator
second_title: Référence de l'API Aspose.Words pour .NET
description: WarningInfoCollection méthode. Renvoie un objet énumérateur qui peut être utilisé pour itérer sur tous les éléments de la collection.
type: docs
weight: 50
url: /fr/net/aspose.words/warninginfocollection/getenumerator/
---
## WarningInfoCollection.GetEnumerator method

Renvoie un objet énumérateur qui peut être utilisé pour itérer sur tous les éléments de la collection.

```csharp
public IEnumerator<WarningInfo> GetEnumerator()
```

### Exemples

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

* class [WarningInfo](../../warninginfo/)
* class [WarningInfoCollection](../)
* espace de noms [Aspose.Words](../../warninginfocollection/)
* Assemblée [Aspose.Words](../../../)


