---
title: FindReplaceOptions.UseLegacyOrder
second_title: Aspose.Words for .NET API Referansı
description: FindReplaceOptions mülk. True metin kutuları dikkate alınarak yukarıdan aşağıya doğru sırayla metin araması yapıldığını belirtir. Varsayılan değerYANLIŞ .
type: docs
weight: 170
url: /tr/net/aspose.words.replacing/findreplaceoptions/uselegacyorder/
---
## FindReplaceOptions.UseLegacyOrder property

True, metin kutuları dikkate alınarak yukarıdan aşağıya doğru sırayla metin araması yapıldığını belirtir. Varsayılan değer:`YANLIŞ` .

```csharp
public bool UseLegacyOrder { get; set; }
```

### Örnekler

Metin bul ve değiştir işlemi gerçekleştirilirken düğümlerin arama sırasının nasıl değiştirileceğini gösterir.

```csharp
public void UseLegacyOrder(bool useLegacyOrder)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Bir regex modeli kullanarak arayabileceğimiz üç çalıştırmayı ekleyin.
    // Bu işlemlerden birini bir metin kutusunun içine yerleştirin.
    builder.Writeln("[tag 1]");
    Shape textBox = builder.InsertShape(ShapeType.TextBox, 100, 50);
    builder.Writeln("[tag 2]");
    builder.MoveTo(textBox.FirstParagraph);
    builder.Write("[tag 3]");

    // Bul ve değiştir işlemini değiştirmek için bir "FindReplaceOptions" nesnesi kullanabiliriz.
    FindReplaceOptions options = new FindReplaceOptions();

    // "ReplacingCallback" özelliğine özel bir geri arama atayın.
    TextReplacementTracker callback = new TextReplacementTracker();
    options.ReplacingCallback = callback;

    // "UseLegacyOrder" özelliğini "true" olarak ayarlarsak,
    // bul ve değiştir işlemi bir metin kutusunun dışındaki tüm işlemleri gerçekleştirecektir
    // metin kutusunun içindekilere geçmeden önce.
    // "UseLegacyOrder" özelliğini "false" olarak ayarlarsak,
    // bul ve değiştir işlemi, bir aralıktaki tüm işlemleri sıralı bir şekilde gerçekleştirecektir.
    options.UseLegacyOrder = useLegacyOrder;

    doc.Range.Replace(new Regex(@"\[tag \d*\]"), "", options);

    Assert.AreEqual(useLegacyOrder ?
        new List<string> { "[tag 1]", "[tag 3]", "[tag 2]" } :
        new List<string> { "[tag 1]", "[tag 2]", "[tag 3]" }, callback.Matches);
}

/// <summary>
/// Bul ve değiştir işlemi sırasında meydana gelen tüm eşleşmelerin sırasını kaydeder.
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
* ad alanı [Aspose.Words.Replacing](../../findreplaceoptions/)
* toplantı [Aspose.Words](../../../)


