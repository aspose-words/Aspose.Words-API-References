---
title: MarkdownLoadOptions.PreserveEmptyLines
linktitle: PreserveEmptyLines
articleTitle: PreserveEmptyLines
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété MarkdownLoadOptions PreserveEmptyLines améliore le chargement de votre document Markdown en préservant les lignes vides pour une meilleure lisibilité.
type: docs
weight: 30
url: /fr/net/aspose.words.loading/markdownloadoptions/preserveemptylines/
---
## MarkdownLoadOptions.PreserveEmptyLines property

Obtient ou définit une valeur booléenne indiquant s'il faut conserver les lignes vides lors du chargement d'unMarkdown document. La valeur par défaut est`FAUX` .

Normalement, les lignes vides entre les éléments de type bloc en Markdown sont ignorées. Les lignes vides au début et à la fin du document sont également ignorées. Cette option permet d'importer ces lignes vides.

```csharp
public bool PreserveEmptyLines { get; set; }
```

## Exemples

Montre comment conserver une ligne vide lors du chargement d'un document.

```csharp
string mdText = $"{Environment.NewLine}Line1{Environment.NewLine}{Environment.NewLine}Line2{Environment.NewLine}{Environment.NewLine}";
using (MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(mdText)))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { PreserveEmptyLines = true };
    Document doc = new Document(stream, loadOptions);

    Assert.AreEqual("\rLine1\r\rLine2\r\f", doc.GetText());
}
```

### Voir également

* class [MarkdownLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
