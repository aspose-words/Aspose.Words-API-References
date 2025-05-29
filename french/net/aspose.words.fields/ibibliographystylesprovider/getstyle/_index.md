---
title: IBibliographyStylesProvider.GetStyle
linktitle: GetStyle
articleTitle: GetStyle
second_title: Aspose.Words pour .NET
description: Découvrez la méthode GetStyle d'IBibliographyStylesProvider pour récupérer et personnaliser sans effort vos styles de bibliographie pour une rédaction académique améliorée.
type: docs
weight: 10
url: /fr/net/aspose.words.fields/ibibliographystylesprovider/getstyle/
---
## IBibliographyStylesProvider.GetStyle method

Renvoie le style de bibliographie.

```csharp
public Stream GetStyle(string styleFileName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| styleFileName | String | Le nom du fichier de style bibliographique. |

### Return_Value

LeStream avec feuille de style XSLT de style bibliographique.

## Remarques

L'implémentation doit renvoyer`nul` pour indiquer que la version MS Word du style spécifié doit être utilisée.

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

* interface [IBibliographyStylesProvider](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
