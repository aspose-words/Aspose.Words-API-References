---
title: FindReplaceOptions.Direction
linktitle: Direction
articleTitle: Direction
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FindReplaceOptions Direction för att anpassa din ersättningsfunktion. Välj mellan Framåt och Bakåt för optimala resultat.
type: docs
weight: 40
url: /sv/net/aspose.words.replacing/findreplaceoptions/direction/
---
## FindReplaceOptions.Direction property

Väljer riktning för ersättning. Standardvärdet ärForward .

```csharp
public FindReplaceDirection Direction { get; set; }
```

## Exempel

Visar hur man avgör vilken riktning en sök-och-ersätt-operation rör sig i dokumentet.

```csharp
public void Direction(FindReplaceDirection findReplaceDirection)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Infoga tre körningar som vi kan söka efter med hjälp av ett regex-mönster.
    // Placera en av dessa körningar i en textruta.
    builder.Writeln("Match 1.");
    builder.Writeln("Match 2.");
    builder.Writeln("Match 3.");
    builder.Writeln("Match 4.");

    // Vi kan använda ett "FindReplaceOptions"-objekt för att modifiera sök-och-ersätt-processen.
    FindReplaceOptions options = new FindReplaceOptions();

    // Tilldela en anpassad återanropning till egenskapen "ReplacingCallback".
    TextReplacementRecorder callback = new TextReplacementRecorder();
    options.ReplacingCallback = callback;

    // Sätt egenskapen "Direction" till "FindReplaceDirection.Backward" för att hämta sök-och-ersätt-funktionen
    // operation för att börja från slutet av intervallet och gå tillbaka till början.
    // Sätt egenskapen "Direction" till "FindReplaceDirection.Forward" för att hämta sök-och-ersätt-funktionen
    // operation för att börja från början av intervallet och gå till slutet.
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
/// Registrerar alla träffar som inträffar under en sök-och-ersätt-operation i den ordning de inträffar.
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

### Se även

* enum [FindReplaceDirection](../../findreplacedirection/)
* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../../)
