---
title: StyleCollection.Document
linktitle: Document
articleTitle: Document
second_title: .NET için Aspose.Words
description: StyleCollection ile sahip belgesine zahmetsizce erişin. Kusursuz belge yönetimini keşfedin ve iş akışınızı bugün geliştirin!
type: docs
weight: 40
url: /tr/net/aspose.words/stylecollection/document/
---
## StyleCollection.Document property

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
* class [StyleCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
