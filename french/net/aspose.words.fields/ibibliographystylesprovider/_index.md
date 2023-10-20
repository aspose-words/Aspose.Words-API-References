---
title: IBibliographyStylesProvider Interface
linktitle: IBibliographyStylesProvider
articleTitle: IBibliographyStylesProvider
second_title: Aspose.Words pour .NET
description: Aspose.Words.Fields.IBibliographyStylesProvider interface. Implémentez cette interface pour fournir un style de bibliographie pour leFieldBibliography etFieldCitation champs lorsquils sont mis à jour en C#.
type: docs
weight: 2670
url: /fr/net/aspose.words.fields/ibibliographystylesprovider/
---
## IBibliographyStylesProvider interface

Implémentez cette interface pour fournir un style de bibliographie pour le[`FieldBibliography`](../fieldbibliography/) et[`FieldCitation`](../fieldcitation/) champs lorsqu'ils sont mis à jour.

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
