---
title: FindReplaceOptions.UseLegacyOrder
linktitle: UseLegacyOrder
articleTitle: UseLegacyOrder
second_title: .NET için Aspose.Words
description: FindReplaceOptions'da UseLegacyOrder özelliğini keşfedin. Daha iyi doğruluk için ardışık metin aramalarını etkinleştirin. Varsayılan değer false'tur. Metin işlemenizi optimize edin!
type: docs
weight: 180
url: /tr/net/aspose.words.replacing/findreplaceoptions/uselegacyorder/
---
## FindReplaceOptions.UseLegacyOrder property

True, metin kutuları dikkate alınarak yukarıdan aşağıya doğru bir metin aramasının gerçekleştirildiğini gösterir. Varsayılan değer`YANLIŞ` .

```csharp
public bool UseLegacyOrder { get; set; }
```

## Örnekler

Bir metin bul ve değiştir işlemi gerçekleştirirken düğümlerin arama sırasının nasıl değiştirileceğini gösterir.

```csharp
public void UseLegacyOrder(bool useLegacyOrder)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Regex desenini kullanarak arayabileceğimiz üç çalışma ekle.
    // Bu çalışmalardan birini metin kutusunun içine yerleştirin.
    builder.Writeln("[tag 1]");
    Shape textBox = builder.InsertShape(ShapeType.TextBox, 100, 50);
    builder.Writeln("[tag 2]");
    builder.MoveTo(textBox.FirstParagraph);
    builder.Write("[tag 3]");

    // Bul ve değiştir işlemini değiştirmek için "FindReplaceOptions" nesnesini kullanabiliriz.
    FindReplaceOptions options = new FindReplaceOptions();

    // "ReplacingCallback" özelliğine özel bir geri arama atayın.
    TextReplacementTracker callback = new TextReplacementTracker();
    options.ReplacingCallback = callback;

    // "UseLegacyOrder" özelliğini "true" olarak ayarlarsak,
    // bul ve değiştir işlemi, metin kutusunun dışındaki tüm çalıştırmaları kapsayacaktır
    // metin kutusunun içindekilere geçmeden önce.
    // "UseLegacyOrder" özelliğini "false" olarak ayarlarsak,
    // bul ve değiştir işlemi, bir aralıktaki tüm çalıştırmaları sıralı bir şekilde inceler.
    options.UseLegacyOrder = useLegacyOrder;

    doc.Range.Replace(new Regex(@"\[tag \d*\]"), "", options);

    Assert.AreEqual(useLegacyOrder ?
        new List<string> { "[tag 1]", "[tag 3]", "[tag 2]" } :
        new List<string> { "[tag 1]", "[tag 2]", "[tag 3]" }, callback.Matches);
}

/// <summary>
/// Bul ve değiştir işlemi sırasında oluşan tüm eşleşmelerin sırasını kaydeder.
/// </summary>
private class TextReplacementTracker : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs e)
    {
        Matches.Add(e.Match.Value);
        return ReplaceAction.Replace;
    }

    public List<string> Matches { get; } = new List<string>();
}
```

### Ayrıca bakınız

* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)
