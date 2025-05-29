---
title: MarkdownLoadOptions.ImportUnderlineFormatting
linktitle: ImportUnderlineFormatting
articleTitle: ImportUnderlineFormatting
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ImportUnderlineFormatting de MarkdownLoadOptions. Contrôlez le formatage du texte souligné avec un simple paramètre booléen. Améliorez votre expérience Markdown !
type: docs
weight: 20
url: /fr/net/aspose.words.loading/markdownloadoptions/importunderlineformatting/
---
## MarkdownLoadOptions.ImportUnderlineFormatting property

Obtient ou définit une valeur booléenne indiquant de reconnaître une séquence de deux caractères plus "++" comme formatage de texte souligné. La valeur par défaut est`FAUX` .

```csharp
public bool ImportUnderlineFormatting { get; set; }
```

## Exemples

Montre comment reconnaître les caractères plus « ++ » comme formatage de texte souligné.

```csharp
using (MemoryStream stream = new MemoryStream(Encoding.ASCII.GetBytes("++12 and B++")))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { ImportUnderlineFormatting = true };
    Document doc = new Document(stream, loadOptions);

    Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
    Assert.AreEqual(Underline.Single, para.Runs[0].Font.Underline);

    loadOptions = new MarkdownLoadOptions() { ImportUnderlineFormatting = false };
    doc = new Document(stream, loadOptions);

    para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
    Assert.AreEqual(Underline.None, para.Runs[0].Font.Underline);
}
```

### Voir également

* class [MarkdownLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
