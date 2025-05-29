---
title: FieldOptions.BibliographyStylesProvider
linktitle: BibliographyStylesProvider
articleTitle: BibliographyStylesProvider
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldOptions BibliographyStylesProvider pour des styles de bibliographie personnalisables, améliorant vos champs FieldBibliography et FieldCitation.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldoptions/bibliographystylesprovider/
---
## FieldOptions.BibliographyStylesProvider property

Obtient ou définit un fournisseur qui renvoie un style de bibliographie pour le[`FieldBibliography`](../../fieldbibliography/) et[`FieldCitation`](../../fieldcitation/) champs.

```csharp
public IBibliographyStylesProvider BibliographyStylesProvider { get; set; }
```

## Exemples

Montre comment remplacer les styles intégrés ou en fournir un personnalisé.

```csharp
public void ChangeBibliographyStyles()
{
    Document doc = new Document(MyDir + "Bibliography.docx");

    // Si le document possède déjà un style, vous pouvez le modifier avec le code suivant :
    // doc.Bibliography.BibliographyStyle = "Style personnalisé de bibliographie.xsl";

    doc.FieldOptions.BibliographyStylesProvider = new BibliographyStylesProvider();
    doc.UpdateFields();

    doc.Save(ArtifactsDir + "Field.ChangeBibliographyStyles.docx");

}

public class BibliographyStylesProvider : IBibliographyStylesProvider
{
    Stream IBibliographyStylesProvider.GetStyle(string styleFileName)
    {
        return File.OpenRead(MyDir + "Bibliography custom style.xsl");
    }
}
```

### Voir également

* interface [IBibliographyStylesProvider](../../ibibliographystylesprovider/)
* class [FieldOptions](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
