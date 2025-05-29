---
title: Style.NextParagraphStyleName
linktitle: NextParagraphStyleName
articleTitle: NextParagraphStyleName
second_title: .NET için Aspose.Words
description: Yeni paragraflar için stil uygulamasını otomatikleştirmek ve belge biçimlendirmenizi geliştirmek amacıyla NextParagraphStyleName özelliğini etkili bir şekilde nasıl kullanacağınızı keşfedin.
type: docs
weight: 140
url: /tr/net/aspose.words/style/nextparagraphstylename/
---
## Style.NextParagraphStyleName property

Belirtilen stille biçimlendirilen bir paragrafından sonra eklenen yeni bir paragrafa otomatik olarak uygulanacak stilin adını alır/ayarlar.

```csharp
public string NextParagraphStyleName { get; set; }
```

## Notlar

Bu özellik Aspose.Words tarafından kullanılmaz. Bir sonraki paragraf stili yalnızca belgeyi MS Word'de düzenlediğinizde otomatik olarak uygulanacaktır.

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
