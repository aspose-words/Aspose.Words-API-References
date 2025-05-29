---
title: IBibliographyStylesProvider Interface
linktitle: IBibliographyStylesProvider
articleTitle: IBibliographyStylesProvider
second_title: Aspose.Words pour .NET
description: Améliorez la mise en forme de votre document avec l'interface Aspose.Words.IBibliographyStylesProvider, parfaite pour personnaliser les styles de bibliographie dans les citations.
type: docs
weight: 3080
url: /fr/net/aspose.words.fields/ibibliographystylesprovider/
---
## IBibliographyStylesProvider interface

Implémentez cette interface pour fournir un style bibliographique pour le[`FieldBibliography`](../fieldbibliography/) et[`FieldCitation`](../fieldcitation/) champs lorsqu'ils sont mis à jour.

```csharp
public interface IBibliographyStylesProvider
```

## Méthodes

| Nom | La description |
| --- | --- |
| [GetStyle](../../aspose.words.fields/ibibliographystylesprovider/getstyle/)(*string*) | Renvoie le style de bibliographie. |

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

* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
