---
title: TxtLeadingSpacesOptions Enum
linktitle: TxtLeadingSpacesOptions
articleTitle: TxtLeadingSpacesOptions
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words TxtLeadingSpacesOptions pour une gestion efficace des espaces de début lors de l'importation de fichiers texte. Optimisez le traitement de vos documents dès aujourd'hui !
type: docs
weight: 4180
url: /fr/net/aspose.words.loading/txtleadingspacesoptions/
---
## TxtLeadingSpacesOptions enumeration

Spécifie les options disponibles pour la gestion des espaces de début lors de l'importation depuisText fichier.

```csharp
public enum TxtLeadingSpacesOptions
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| ConvertToIndent | `0` | Les espaces de début sont supprimés et convertis en retrait à gauche. |
| Trim | `1` | Les espaces de début sont supprimés |
| Preserve | `2` | Les espaces de début sont conservés. |

## Exemples

Montre comment couper les espaces blancs lors du chargement de documents en texte brut.

```csharp
string textDoc = "      Line 1 \n" +
                 "    Line 2   \n" +
                 " Line 3       ";

// Créer un objet « TxtLoadOptions », que nous pouvons transmettre au constructeur d'un document
// pour modifier la façon dont nous chargeons un document en texte brut.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Définissez la propriété « LeadingSpacesOptions » sur « TxtLeadingSpacesOptions.Preserve »
// pour conserver tous les caractères d'espacement au début de chaque ligne.
// Définissez la propriété « LeadingSpacesOptions » sur « TxtLeadingSpacesOptions.ConvertToIndent »
// pour supprimer tous les caractères d'espacement du début de chaque ligne,
// puis appliquez un retrait de première ligne à gauche au paragraphe pour simuler l'effet des espaces.
// Définissez la propriété « LeadingSpacesOptions » sur « TxtLeadingSpacesOptions.Trim »
// pour supprimer tous les caractères d'espacement du début de chaque ligne.
loadOptions.LeadingSpacesOptions = txtLeadingSpacesOptions;

// Définissez la propriété « TrailingSpacesOptions » sur « TxtTrailingSpacesOptions.Preserve »
 // pour conserver tous les caractères d'espacement à la fin de chaque ligne.
 // Définissez la propriété « TrailingSpacesOptions » sur « TxtTrailingSpacesOptions.Trim » pour
// supprimez tous les caractères d'espacement de la fin de chaque ligne.
loadOptions.TrailingSpacesOptions = txtTrailingSpacesOptions;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(textDoc)), loadOptions);
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

switch (txtLeadingSpacesOptions)
{
    case TxtLeadingSpacesOptions.ConvertToIndent:
        Assert.AreEqual(37.8d, paragraphs[0].ParagraphFormat.FirstLineIndent);
        Assert.AreEqual(25.2d, paragraphs[1].ParagraphFormat.FirstLineIndent);
        Assert.AreEqual(6.3d, paragraphs[2].ParagraphFormat.FirstLineIndent);

        Assert.True(paragraphs[0].GetText().StartsWith("Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith("Line 3"));
        break;
    case TxtLeadingSpacesOptions.Preserve:
        Assert.True(paragraphs.All(p => ((Paragraph)p).ParagraphFormat.FirstLineIndent == 0.0d));

        Assert.True(paragraphs[0].GetText().StartsWith("      Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("    Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith(" Line 3"));
        break;
    case TxtLeadingSpacesOptions.Trim:
        Assert.True(paragraphs.All(p => ((Paragraph)p).ParagraphFormat.FirstLineIndent == 0.0d));

        Assert.True(paragraphs[0].GetText().StartsWith("Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith("Line 3"));
        break;
}

switch (txtTrailingSpacesOptions)
{
    case TxtTrailingSpacesOptions.Preserve:
        Assert.True(paragraphs[0].GetText().EndsWith("Line 1 \r"));
        Assert.True(paragraphs[1].GetText().EndsWith("Line 2   \r"));
        Assert.True(paragraphs[2].GetText().EndsWith("Line 3       \f"));
        break;
    case TxtTrailingSpacesOptions.Trim:
        Assert.True(paragraphs[0].GetText().EndsWith("Line 1\r"));
        Assert.True(paragraphs[1].GetText().EndsWith("Line 2\r"));
        Assert.True(paragraphs[2].GetText().EndsWith("Line 3\f"));
        break;
}
```

### Voir également

* espace de noms [Aspose.Words.Loading](../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../)
