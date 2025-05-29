---
title: Style.Styles
linktitle: Styles
articleTitle: Styles
second_title: .NET için Aspose.Words
description: Tasarımınızı benzersiz ve tutarlı bir estetikle zenginleştirerek özenle seçilmiş bir stil koleksiyonuna erişmek için Stil Stilleri özelliğini keşfedin.
type: docs
weight: 190
url: /tr/net/aspose.words/style/styles/
---
## Style.Styles property

Bu stilin ait olduğu stil koleksiyonunu alır.

```csharp
public StyleCollection Styles { get; }
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

* class [StyleCollection](../../stylecollection/)
* class [Style](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
