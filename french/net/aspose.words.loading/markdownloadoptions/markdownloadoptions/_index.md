---
title: MarkdownLoadOptions
linktitle: MarkdownLoadOptions
articleTitle: MarkdownLoadOptions
second_title: Aspose.Words pour .NET
description: Découvrez le constructeur MarkdownLoadOptions pour initialiser facilement les instances MarkdownLoadOptions pour un traitement et une personnalisation améliorés des documents.
type: docs
weight: 10
url: /fr/net/aspose.words.loading/markdownloadoptions/markdownloadoptions/
---
## MarkdownLoadOptions constructor

Initialise une nouvelle instance de[`MarkdownLoadOptions`](../) classe.

```csharp
public MarkdownLoadOptions()
```

## Remarques

Définit automatiquement[`LoadFormat`](../../../aspose.words/loadformat/) àMarkdown .

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
