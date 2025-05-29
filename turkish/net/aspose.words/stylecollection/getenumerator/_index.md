---
title: StyleCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: .NET için Aspose.Words
description: Stilleri adlarına göre alfabetik olarak zahmetsizce listelemek için StyleCollection GetEnumerator metodunu keşfedin. Kodlama verimliliğinizi bugün artırın!
type: docs
weight: 90
url: /tr/net/aspose.words/stylecollection/getenumerator/
---
## StyleCollection.GetEnumerator method

Stilleri adlarının alfabetik sırasına göre numaralandıracak bir numaralandırıcı nesnesi alır.

```csharp
public IEnumerator<Style> GetEnumerator()
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

* class [Style](../../style/)
* class [StyleCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
