---
title: FindReplaceOptions.Direction
linktitle: Direction
articleTitle: Direction
second_title: .NET için Aspose.Words
description: Değiştirme işlevinizi özelleştirmek için FindReplaceOptions Direction özelliğini keşfedin. En iyi sonuçlar için İleri ve Geri arasında seçim yapın.
type: docs
weight: 40
url: /tr/net/aspose.words.replacing/findreplaceoptions/direction/
---
## FindReplaceOptions.Direction property

Değiştirme yönünü seçer. Varsayılan değerForward .

```csharp
public FindReplaceDirection Direction { get; set; }
```

## Örnekler

Bir bul ve değiştir işleminin belgeyi hangi yönde dolaşacağının nasıl belirleneceğini gösterir.

```csharp
public void Direction(FindReplaceDirection findReplaceDirection)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Regex desenini kullanarak arayabileceğimiz üç çalışma ekle.
    // Bu çalışmalardan birini metin kutusunun içine yerleştirin.
    builder.Writeln("Match 1.");
    builder.Writeln("Match 2.");
    builder.Writeln("Match 3.");
    builder.Writeln("Match 4.");

    // Bul ve değiştir işlemini değiştirmek için "FindReplaceOptions" nesnesini kullanabiliriz.
    FindReplaceOptions options = new FindReplaceOptions();

    // "ReplacingCallback" özelliğine özel bir geri arama atayın.
    TextReplacementRecorder callback = new TextReplacementRecorder();
    options.ReplacingCallback = callback;

    // Bul ve değiştir özelliğini elde etmek için "Direction" özelliğini "FindReplaceDirection.Backward" olarak ayarlayın
    // aralığın sonundan başlayıp başa doğru gitme işlemi.
    // Bul ve değiştir özelliğini elde etmek için "Direction" özelliğini "FindReplaceDirection.Forward" olarak ayarlayın
    // aralığın başlangıcından başlayıp sonuna kadar gitme işlemi.
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
/// Bir bul-değiştir işlemi sırasında gerçekleşen tüm eşleşmeleri, gerçekleştikleri sırayla kaydeder.
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
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)
