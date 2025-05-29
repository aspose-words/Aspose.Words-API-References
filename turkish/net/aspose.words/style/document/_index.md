---
title: Style.Document
linktitle: Document
articleTitle: Document
second_title: .NET için Aspose.Words
description: Gelişmiş organizasyon ve verimlilik için sahip olduğunuz belgelere kolayca erişmek ve bunları yönetmek amacıyla Stil Belgesi özelliğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words/style/document/
---
## Style.Document property

Sahip belgesini alır.

```csharp
public DocumentBase Document { get; }
```

## Örnekler

Bir belgenin stil koleksiyonuna nasıl erişileceğini gösterir.

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// Aspose.Words kullanılarak oluşturulan bir belgenin varsayılan olarak içerdiği tüm stilleri sayın ve listeleyin.
using (IEnumerator<Style> stylesEnum = doc.Styles.GetEnumerator())
{
    while (stylesEnum.MoveNext())
    {
        Style curStyle = stylesEnum.Current;
        Console.WriteLine($"Style name:\t\"{curStyle.Name}\", of type \"{curStyle.Type}\"");
        Console.WriteLine($"\tSubsequent style:\t{curStyle.NextParagraphStyleName}");
        Console.WriteLine($"\tIs heading:\t\t\t{curStyle.IsHeading}");
        Console.WriteLine($"\tIs QuickStyle:\t\t{curStyle.IsQuickStyle}");

        Assert.AreEqual(doc, curStyle.Document);
    }
}
```

### Ayrıca bakınız

* class [DocumentBase](../../documentbase/)
* class [Style](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
