---
title: FindReplaceDirection
second_title: Aspose.Words for .NET API Referansı
description: Değiştirme işlemlerinin yönünü belirtir.
type: docs
weight: 4350
url: /tr/net/aspose.words.replacing/findreplacedirection/
---
## FindReplaceDirection enumeration

Değiştirme işlemlerinin yönünü belirtir.

```csharp
public enum FindReplaceDirection
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Forward | `0` | Eşleşen öğeler birinciden sonuncuya değiştirilir. |
| Backward | `1` | Eşleşen öğeler, sondan başa doğru değiştirilir. |

### Örnekler

Bir bul ve değiştir işleminin belgeyi hangi yönde kat edeceğinin nasıl belirleneceğini gösterir.

```csharp
public void Direction(FindReplaceDirection findReplaceDirection)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normal ifade kalıbı kullanarak arayabileceğimiz üç çalıştırma ekleyin.
    // Bu çalıştırmalardan birini bir metin kutusuna yerleştirin.
    builder.Writeln("Match 1.");
    builder.Writeln("Match 2.");
    builder.Writeln("Match 3.");
    builder.Writeln("Match 4.");

    // Bul ve değiştir işlemini değiştirmek için bir "FindReplaceOptions" nesnesi kullanabiliriz.
    FindReplaceOptions options = new FindReplaceOptions();

    // "ReplacecingCallback" özelliğine özel bir geri arama atayın.
    TextReplacementRecorder callback = new TextReplacementRecorder();
    options.ReplacingCallback = callback;

    // Bul ve değiştir özelliğini almak için "Yön" özelliğini "FindReplaceDirection.Backward" olarak ayarlayın
    // aralığın sonundan başlayıp başa dönme işlemi.
    // Bul ve değiştir özelliğini almak için "Yön" özelliğini "FindReplaceDirection.Backward" olarak ayarlayın
    // aralığın başından başlayıp sonuna doğru hareket etme işlemi.
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
/// Bul ve değiştir işlemi sırasında gerçekleşen tüm eşleşmeleri gerçekleştikleri sırayla kaydeder.
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

* ad alanı [Aspose.Words.Replacing](../../aspose.words.replacing)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
