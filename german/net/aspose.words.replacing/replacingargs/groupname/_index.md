---
title: ReplacingArgs.GroupName
linktitle: GroupName
articleTitle: GroupName
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie die GroupName-Eigenschaft effektiv nutzen, um erfasste Gruppen in Ihren Übereinstimmungen durch benutzerdefinierte Zeichenfolgen zu ersetzen. Verbessern Sie Ihre Fähigkeiten zur Zeichenfolgenmanipulation!
type: docs
weight: 20
url: /de/net/aspose.words.replacing/replacingargs/groupname/
---
## ReplacingArgs.GroupName property

Identifiziert anhand des Namens eine erfasste Gruppe in der[`Match`](../match/) , das durch das ersetzt werden soll[`Replacement`](../replacement/) Zeichenfolge.

```csharp
public string GroupName { get; set; }
```

## Bemerkungen

Wenn der Gruppenname`null` ,[`GroupIndex`](../groupindex/) wird zur Identifizierung der Gruppe verwendet.

Standard ist`null`.

## Beispiele

Zeigt, wie Sie über FindReplaceOptions eine andere Schriftart auf neuen Inhalt anwenden.

```csharp
public void ConvertNumbersToHexadecimal()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Arial";
    builder.Writeln("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\n" +
                    "123, 456, 789 and 17379.");

    // Wir können ein „FindReplaceOptions“-Objekt verwenden, um den Suchen-und-Ersetzen-Prozess zu ändern.
    FindReplaceOptions options = new FindReplaceOptions();

    // Legen Sie die Eigenschaft „HighlightColor“ auf eine Hintergrundfarbe fest, die wir auf den resultierenden Text der Operation anwenden möchten.
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
/// Ersetzt numerische Such- und Ersetzungsübereinstimmungen durch ihre hexadezimalen Entsprechungen.
/// Führt ein Protokoll über jeden Austausch.
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

### Siehe auch

* class [ReplacingArgs](../)
* namensraum [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Montage [Aspose.Words](../../../)
