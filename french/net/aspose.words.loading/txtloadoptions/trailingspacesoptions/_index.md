---
title: TxtLoadOptions.TrailingSpacesOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: TxtLoadOptions propriété. Obtient ou définit loption préférée de gestion des espaces de fin. La valeur par défaut estTrim .
type: docs
weight: 50
url: /fr/net/aspose.words.loading/txtloadoptions/trailingspacesoptions/
---
## TxtLoadOptions.TrailingSpacesOptions property

Obtient ou définit l'option préférée de gestion des espaces de fin. La valeur par défaut estTrim .

```csharp
public TxtTrailingSpacesOptions TrailingSpacesOptions { get; set; }
```

### Exemples

Montre comment couper les espaces blancs lors du chargement de documents en texte brut.

```csharp
string textDoc = "      Line 1 \n" +
                 "    Line 2   \n" +
                 " Line 3       ";

// Crée un objet "TxtLoadOptions", que nous pouvons passer au constructeur d'un document
// pour modifier la façon dont nous chargeons un document en clair.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Définissez la propriété "LeadingSpacesOptions" sur "TxtLeadingSpacesOptions.Preserve"
// pour conserver tous les caractères d'espacement au début de chaque ligne.
// Définissez la propriété "LeadingSpacesOptions" sur "TxtLeadingSpacesOptions.ConvertToIndent"
// pour supprimer tous les caractères d'espacement du début de chaque ligne,
// puis appliquez un retrait de première ligne à gauche au paragraphe pour simuler l'effet des espaces.
// Définissez la propriété "LeadingSpacesOptions" sur "TxtLeadingSpacesOptions.Trim"
// pour supprimer tous les caractères d'espacement du début de chaque ligne.
loadOptions.LeadingSpacesOptions = txtLeadingSpacesOptions;

// Définissez la propriété "TrailingSpacesOptions" sur "TxtTrailingSpacesOptions.Preserve"
// pour conserver tous les caractères d'espacement à la fin de chaque ligne. 
// Définissez la propriété "TrailingSpacesOptions" sur "TxtTrailingSpacesOptions.Trim" pour 
// supprime tous les caractères d'espacement à la fin de chaque ligne.
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

* enum [TxtTrailingSpacesOptions](../../txttrailingspacesoptions/)
* class [TxtLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../txtloadoptions/)
* Assemblée [Aspose.Words](../../../)


