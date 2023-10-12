---
title: FindReplaceOptions.Direction
second_title: Aspose.Words for .NET API Referansı
description: FindReplaceOptions mülk. Değiştirme yönünü seçer. Varsayılan değerForward .
type: docs
weight: 40
url: /tr/net/aspose.words.replacing/findreplaceoptions/direction/
---
## FindReplaceOptions.Direction property

Değiştirme yönünü seçer. Varsayılan değer:Forward .

```csharp
public FindReplaceDirection Direction { get; set; }
```

### Örnekler

Bul ve değiştir işleminin belgeyi hangi yönde geçeceğinin nasıl belirleneceğini gösterir.

```csharp
public void Direction(FindReplaceDirection findReplaceDirection)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Bir regex modeli kullanarak arayabileceğimiz üç çalıştırmayı ekleyin.
    // Bu işlemlerden birini bir metin kutusunun içine yerleştirin.
    builder.Writeln("Match 1.");
    builder.Writeln("Match 2.");
    builder.Writeln("Match 3.");
    builder.Writeln("Match 4.");

    // Bul ve değiştir işlemini değiştirmek için bir "FindReplaceOptions" nesnesi kullanabiliriz.
    FindReplaceOptions options = new FindReplaceOptions();

    // "ReplacingCallback" özelliğine özel bir geri arama atayın.
    TextReplacementRecorder callback = new TextReplacementRecorder();
    options.ReplacingCallback = callback;

    // Bul ve değiştir işlevini elde etmek için "Direction" özelliğini "FindReplaceDirection.Backward" olarak ayarlayın
    // aralığın sonundan başlayıp başlangıca geri dönme işlemi.
    // Bul ve değiştir işlevini elde etmek için "Direction" özelliğini "FindReplaceDirection.Backward" olarak ayarlayın
    // aralığın başından başlayıp sonuna kadar ilerleme işlemi.
    options.Direction = findReplaceDirection;

    doc.Range.Replace(new Regex(@"Match \d*"), "Replacement", options);

    Assert.AreEqual("Replacement.\r" +
                    "Replacement.\r" +
                    "Replacement.\r" +
                    "Replacement.", doc.GetText().Trim());

    switch (findReplaceDirection)
    {
        case FindReplaceDirection.Forward:
            Assert.AreEqual(new[] { "Match 1", "Match 2", "Match 3", "Match 4" }, callback.Matches);
            break;
        case FindReplaceDirection.Backward:
            Assert.AreEqual(new[] { "Match 4", "Match 3", "Match 2", "Match 1" }, callback.Matches);
            break;
    }
}

/// <summary>
/// Bul ve değiştir işlemi sırasında meydana gelen tüm eşleşmeleri gerçekleşme sırasına göre kaydeder.
/// </summary>
private class TextReplacementRecorder : IReplacingCallback
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

* enum [FindReplaceDirection](../../findreplacedirection/)
* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../findreplaceoptions/)
* toplantı [Aspose.Words](../../../)


