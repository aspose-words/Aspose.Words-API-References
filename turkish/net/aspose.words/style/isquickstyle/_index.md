---
title: Style.IsQuickStyle
linktitle: IsQuickStyle
articleTitle: IsQuickStyle
second_title: .NET için Aspose.Words
description: IsQuickStyle özelliğinin, Hızlı Stil galerisinde stilleri sergileyerek kolay erişim ve gelişmiş iş akışı sağlayarak MS Word deneyiminizi nasıl geliştirdiğini keşfedin.
type: docs
weight: 80
url: /tr/net/aspose.words/style/isquickstyle/
---
## Style.IsQuickStyle property

Bu stilin MS Word UI içindeki Hızlı Stil galerisinde gösterilip gösterilmeyeceğini belirtir.

```csharp
public bool IsQuickStyle { get; set; }
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
