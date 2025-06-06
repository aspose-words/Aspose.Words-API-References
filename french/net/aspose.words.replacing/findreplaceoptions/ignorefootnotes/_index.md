---
title: FindReplaceOptions.IgnoreFootnotes
linktitle: IgnoreFootnotes
articleTitle: IgnoreFootnotes
second_title: Aspose.Words pour .NET
description: Découvrez la propriété IgnoreFootnotes de FindReplaceOptions pour gérer facilement les notes de bas de page dans vos documents. Améliorez l'efficacité de vos modifications grâce à cette simple option !
type: docs
weight: 90
url: /fr/net/aspose.words.replacing/findreplaceoptions/ignorefootnotes/
---
## FindReplaceOptions.IgnoreFootnotes property

Obtient ou définit une valeur booléenne indiquant d'ignorer les notes de bas de page. La valeur par défaut est`FAUX` .

```csharp
public bool IgnoreFootnotes { get; set; }
```

## Exemples

Montre comment ignorer les notes de bas de page lors d'une opération de recherche et de remplacement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Footnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder.InsertParagraph();

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Endnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// Définissez l'indicateur « IgnoreFootnotes » sur « true » pour obtenir la fonction de recherche et de remplacement
// opération pour ignorer le texte à l'intérieur des notes de bas de page.
// Définissez l'indicateur « IgnoreFootnotes » sur « false » pour obtenir la fonction de recherche et de remplacement
// opération permettant également de rechercher du texte à l'intérieur des notes de bas de page.
FindReplaceOptions options = new FindReplaceOptions { IgnoreFootnotes = isIgnoreFootnotes };
doc.Range.Replace("Lorem ipsum", "Replaced Lorem ipsum", options);
```

### Voir également

* class [FindReplaceOptions](../)
* espace de noms [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Assemblée [Aspose.Words](../../../)
