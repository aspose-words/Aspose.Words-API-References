---
title: ReplacingArgs.Match
second_title: Référence de l'API Aspose.Words pour .NET
description: ReplacingArgs propriété. LeMatch résultant dune seule correspondance dexpression regular lors dune Remplacer .
type: docs
weight: 30
url: /fr/net/aspose.words.replacing/replacingargs/match/
---
## ReplacingArgs.Match property

LeMatch résultant d'une seule correspondance d'expression regular lors d'une **Remplacer** .

```csharp
public Match Match { get; }
```

### Remarques

**Match.Index"** obtient la position de départ de base zéro de la correspondance à partir du début de la plage de recherche et de remplacement.

### Exemples

Montre comment appliquer une police différente à un nouveau contenu via FindReplaceOptions.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Arial";
    builder.Writeln("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\n" +
                    "123, 456, 789 and 17379.");

    // Nous pouvons utiliser un objet "FindReplaceOptions" pour modifier le processus de recherche et de remplacement.
    FindReplaceOptions options = new FindReplaceOptions();

    // Définissez la propriété "HighlightColor" sur une couleur d'arrière-plan que nous voulons appliquer au texte résultant de l'opération.
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
/// Remplace les correspondances numériques de recherche et de remplacement par leurs équivalents hexadécimaux.
/// Maintient un journal de chaque remplacement.
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

### Voir également

* class [ReplacingArgs](../)
* espace de noms [Aspose.Words.Replacing](../../replacingargs/)
* Assemblée [Aspose.Words](../../../)


