---
title: Style.IsHeading
linktitle: IsHeading
articleTitle: IsHeading
second_title: .NET için Aspose.Words
description: IsHeading özelliğini keşfedin. Bir stilin yerleşik bir Başlık stili olup olmadığını kolayca belirleyerek belgenizin yapısını ve okunabilirliğini artırın.
type: docs
weight: 70
url: /tr/net/aspose.words/style/isheading/
---
## Style.IsHeading property

Stil yerleşik Başlık stillerinden biri olduğunda doğrudur.

```csharp
public bool IsHeading { get; }
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

* class [Style](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
