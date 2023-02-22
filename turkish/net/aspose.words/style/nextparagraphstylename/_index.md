---
title: Style.NextParagraphStyleName
second_title: Aspose.Words for .NET API Referansı
description: Style mülk. Belirtilen stille biçimlendirilmiş a paragrafından sonra eklenen yeni paragrafa otomatik olarak uygulanacak stilin adını alır/ayarlar.
type: docs
weight: 120
url: /tr/net/aspose.words/style/nextparagraphstylename/
---
## Style.NextParagraphStyleName property

Belirtilen stille biçimlendirilmiş a paragrafından sonra eklenen yeni paragrafa otomatik olarak uygulanacak stilin adını alır/ayarlar.

```csharp
public string NextParagraphStyleName { get; set; }
```

### Notlar

Bu özellik Aspose.Words tarafından kullanılmaz. Belgeyi MS Word'de düzenlediğinizde, sonraki paragraf stili yalnızca otomatik olarak uygulanacaktır.

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

* class [Style](../)
* ad alanı [Aspose.Words](../../style/)
* toplantı [Aspose.Words](../../../)


