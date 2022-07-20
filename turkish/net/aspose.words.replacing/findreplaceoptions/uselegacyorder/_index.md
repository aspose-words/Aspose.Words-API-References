---
title: UseLegacyOrder
second_title: Aspose.Words for .NET API Referansı
description: True bir metin aramasının metin kutuları dikkate alınarak yukarıdan aşağıya sırayla gerçekleştirildiğini belirtir. Varsayılan değer falsedir.
type: docs
weight: 150
url: /tr/net/aspose.words.replacing/findreplaceoptions/uselegacyorder/
---
## FindReplaceOptions.UseLegacyOrder property

True, bir metin aramasının metin kutuları dikkate alınarak yukarıdan aşağıya sırayla gerçekleştirildiğini belirtir. Varsayılan değer false'dir.

```csharp
public bool UseLegacyOrder { get; set; }
```

### Örnekler

Metin bul ve değiştir işlemi gerçekleştirirken düğümlerin arama sırasının nasıl değiştirileceğini gösterir.

```csharp
[TestCase(true)] // ExAtla
[TestCase(false)] // ExAtla
public void UseLegacyOrder(bool useLegacyOrder)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normal ifade kalıbı kullanarak arayabileceğimiz üç çalıştırma ekleyin.
    // Bu çalıştırmalardan birini bir metin kutusuna yerleştirin.
    builder.Writeln("[tag 1]");
    Shape textBox = builder.InsertShape(ShapeType.TextBox, 100, 50);
    builder.Writeln("[tag 2]");
    builder.MoveTo(textBox.FirstParagraph);
    builder.Write("[tag 3]");

    // Bul ve değiştir işlemini değiştirmek için bir "FindReplaceOptions" nesnesi kullanabiliriz.
    FindReplaceOptions options = new FindReplaceOptions();

    // "ReplacecingCallback" özelliğine özel bir geri arama atayın.
    TextReplacementTracker callback = new TextReplacementTracker();
    options.ReplacingCallback = callback;

    // "UseLegacyOrder" özelliğini "true" olarak ayarlarsak,
    // bul ve değiştir işlemi, bir metin kutusunun dışındaki tüm çalıştırmalardan geçecek
    // bir metin kutusu içindekilerden geçmeden önce.
    // "UseLegacyOrder" özelliğini "false" olarak ayarlarsak,
    // bul ve değiştir işlemi, bir aralıktaki tüm çalıştırmaları sıralı olarak gözden geçirecektir.
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

* class [FindReplaceOptions](../../findreplaceoptions)
* ad alanı [Aspose.Words.Replacing](../../findreplaceoptions)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->