---
title: ReplacingArgs.Match
linktitle: Match
articleTitle: Match
second_title: .NET için Aspose.Words
description: Sorunsuz regex değiştirmeleri için ReplacingArgs Match özelliğini keşfedin. Kesin eşleşme sonuçlarıyla kodlama verimliliğinizi artırın!
type: docs
weight: 30
url: /tr/net/aspose.words.replacing/replacingargs/match/
---
## ReplacingArgs.Match property

Match bir regular ifadesinin eşleşmesinden kaynaklanan**Yer değiştirmek** .

```csharp
public Match Match { get; }
```

## Notlar

**Eşleşme.İndeks"** Bul ve değiştir aralığının başlangıcından itibaren eşleşmenin sıfırdan başlayan starting konumunu alır.

## Örnekler

FindReplaceOptions aracılığıyla yeni içeriğe farklı bir yazı tipinin nasıl uygulanacağını gösterir.

```csharp
public void ConvertNumbersToHexadecimal()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Arial";
    builder.Writeln("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\n" +
                    "123, 456, 789 and 17379.");

    // Bul ve değiştir işlemini değiştirmek için "FindReplaceOptions" nesnesini kullanabiliriz.
    FindReplaceOptions options = new FindReplaceOptions();

    // "HighlightColor" özelliğini, işlemin sonuç metnine uygulamak istediğimiz bir arka plan rengine ayarlayın.
    options.ApplyFont.HighlightColor = Color.LightGray;

    NumberHexer numberHexer = new NumberHexer();
    options.ReplacingCallback = numberHexer;

    int replacementCount = doc.Range.Replace(new Regex("[0-9]+"), "", options);

    Console.WriteLine(numberHexer.GetLog());

    Assert.AreEqual(4, replacementCount);
    Assert.AreEqual("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\r" +
                    "0x7B, 0x1C8, 0x315 and 0x43E3.", doc.GetText().Trim());
    Assert.AreEqual(4, doc.GetChildNodes(NodeType.Run, true).OfType<Run>()
            .Count(r => r.Font.HighlightColor.ToArgb() == Color.LightGray.ToArgb()));
}

/// <summary>
/// Sayısal bul-değiştir eşleşmelerini onaltılık eşdeğerleriyle değiştirir.
/// Her değişimin kaydını tutar.
/// </summary>
private class NumberHexer : IReplacingCallback
{
    public ReplaceAction Replacing(ReplacingArgs args)
    {
        mCurrentReplacementNumber++;

        int number = Convert.ToInt32(args.Match.Value);

        args.Replacement = $"0x{number:X}";

        mLog.AppendLine($"Match #{mCurrentReplacementNumber}");
        mLog.AppendLine($"\tOriginal value:\t{args.Match.Value}");
        mLog.AppendLine($"\tReplacement:\t{args.Replacement}");
        mLog.AppendLine($"\tOffset in parent {args.MatchNode.NodeType} node:\t{args.MatchOffset}");

        mLog.AppendLine(string.IsNullOrEmpty(args.GroupName)
            ? $"\tGroup index:\t{args.GroupIndex}"
            : $"\tGroup name:\t{args.GroupName}");

        return ReplaceAction.Replace;
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private int mCurrentReplacementNumber;
    private readonly StringBuilder mLog = new StringBuilder();
}
```

### Ayrıca bakınız

* class [ReplacingArgs](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)
