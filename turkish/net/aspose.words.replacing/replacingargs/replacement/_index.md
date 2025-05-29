---
title: ReplacingArgs.Replacement
linktitle: Replacement
articleTitle: Replacement
second_title: .NET için Aspose.Words
description: Gelişmiş kodlama verimliliği için değiştirme dizelerinizi kolayca yönetmek ve özelleştirmek amacıyla ReplacingArgs Değiştirme özelliğini keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words.replacing/replacingargs/replacement/
---
## ReplacingArgs.Replacement property

Değiştirme dizesini alır veya ayarlar.

```csharp
public string Replacement { get; set; }
```

## Örnekler

Tüm değiştirmeleri izlerken, düzenli ifade deseninin tüm oluşumlarının başka bir dizeyle nasıl değiştirileceğini gösterir.

```csharp
public void ReplaceWithCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // Bul ve değiştir işlemini değiştirmek için "FindReplaceOptions" nesnesini kullanabiliriz.
    FindReplaceOptions options = new FindReplaceOptions();

    // "Değiştir" yönteminin yapacağı tüm değişiklikleri izleyen bir geri çağırma ayarlayın.
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// Bir bul-değiştir işlemi tarafından yapılan her metin değişiminin günlüğünü tutar
/// ve orijinal eşleşen metnin değerini not eder.
/// </summary>
private class TextFindAndReplacementLogger : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        mLog.AppendLine($"\"{args.Match.Value}\" converted to \"{args.Replacement}\" " +
                        $"{args.MatchOffset} characters into a {args.MatchNode.NodeType} node.");

        args.Replacement = $"(Old value:\"{args.Match.Value}\") {args.Replacement}";
        return ReplaceAction.Replace;
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private readonly StringBuilder mLog = new StringBuilder();
}
```

### Ayrıca bakınız

* class [ReplacingArgs](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)
