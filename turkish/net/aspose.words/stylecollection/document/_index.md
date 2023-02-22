---
title: StyleCollection.Document
second_title: Aspose.Words for .NET API Referansı
description: StyleCollection mülk. Sahip belgesini alır.
type: docs
weight: 40
url: /tr/net/aspose.words/stylecollection/document/
---
## StyleCollection.Document property

Sahip belgesini alır.

```csharp
public DocumentBase Document { get; }
```

### Örnekler

Bir belgenin stil koleksiyonuna nasıl erişileceğini gösterir.

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// Aspose.Words kullanılarak oluşturulan bir belgenin varsayılan olarak içerdiği tüm stilleri numaralandırın ve listeleyin.
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
* class [StyleCollection](../)
* ad alanı [Aspose.Words](../../stylecollection/)
* toplantı [Aspose.Words](../../../)


