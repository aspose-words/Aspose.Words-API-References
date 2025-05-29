---
title: Bibliography.BibliographyStyle
linktitle: BibliographyStyle
articleTitle: BibliographyStyle
second_title: Aspose.Words pour .NET
description: Découvrez la propriété BibliographyStyle pour gérer et personnaliser facilement le style actif de votre bibliographie pour une organisation et une présentation améliorées.
type: docs
weight: 10
url: /fr/net/aspose.words.bibliography/bibliography/bibliographystyle/
---
## Bibliography.BibliographyStyle property

Obtient ou définit une chaîne qui représente le nom du style actif à utiliser pour une bibliographie.

```csharp
public string BibliographyStyle { get; set; }
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

* class [Bibliography](../)
* espace de noms [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* Assemblée [Aspose.Words](../../../)
