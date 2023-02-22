---
title: FindReplaceOptions.IgnoreFootnotes
second_title: Référence de l'API Aspose.Words pour .NET
description: FindReplaceOptions propriété. Obtient ou définit une valeur booléenne indiquant soit dignorer les notes de bas de page. La valeur par défaut estfaux .
type: docs
weight: 90
url: /fr/net/aspose.words.replacing/findreplaceoptions/ignorefootnotes/
---
## FindReplaceOptions.IgnoreFootnotes property

Obtient ou définit une valeur booléenne indiquant soit d'ignorer les notes de bas de page. La valeur par défaut est`faux` .

```csharp
public bool IgnoreFootnotes { get; set; }
```

### Exemples

Montre comment ignorer les notes de bas de page lors d'une opération de recherche et de remplacement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Footnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder.InsertParagraph();

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Endnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// Définissez le drapeau "IgnoreFootnotes" sur "true" pour obtenir la recherche et le remplacement
// opération pour ignorer le texte à l'intérieur des notes de bas de page.
// Définissez le drapeau "IgnoreFootnotes" sur "false" pour obtenir le rechercher-et-remplacer
// opération pour rechercher également du texte dans les notes de bas de page.
FindReplaceOptions options = new FindReplaceOptions { IgnoreFootnotes = isIgnoreFootnotes };
doc.Range.Replace("Lorem ipsum", "Replaced Lorem ipsum", options);
```

### Voir également

* class [FindReplaceOptions](../)
* espace de noms [Aspose.Words.Replacing](../../findreplaceoptions/)
* Assemblée [Aspose.Words](../../../)


