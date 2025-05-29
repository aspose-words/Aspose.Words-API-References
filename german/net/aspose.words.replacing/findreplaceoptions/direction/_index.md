---
title: FindReplaceOptions.Direction
linktitle: Direction
articleTitle: Direction
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FindReplaceOptions Direction“, um Ihre Ersetzungsfunktion anzupassen. Wählen Sie zwischen „Vorwärts“ und „Rückwärts“ für optimale Ergebnisse.
type: docs
weight: 40
url: /de/net/aspose.words.replacing/findreplaceoptions/direction/
---
## FindReplaceOptions.Direction property

Wählt die Richtung für das Ersetzen. Der Standardwert istForward .

```csharp
public FindReplaceDirection Direction { get; set; }
```

## Beispiele

Zeigt, wie ermittelt wird, in welche Richtung ein Suchen-und-Ersetzen-Vorgang das Dokument durchläuft.

```csharp
public void Direction(FindReplaceDirection findReplaceDirection)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Fügen Sie drei Läufe ein, nach denen wir mithilfe eines Regex-Musters suchen können.
    // Platzieren Sie einen dieser Läufe in einem Textfeld.
    builder.Writeln("Match 1.");
    builder.Writeln("Match 2.");
    builder.Writeln("Match 3.");
    builder.Writeln("Match 4.");

    // Wir können ein „FindReplaceOptions“-Objekt verwenden, um den Suchen-und-Ersetzen-Prozess zu ändern.
    FindReplaceOptions options = new FindReplaceOptions();

    // Weisen Sie der Eigenschaft „ReplacingCallback“ einen benutzerdefinierten Rückruf zu.
    TextReplacementRecorder callback = new TextReplacementRecorder();
    options.ReplacingCallback = callback;

    // Setzen Sie die Eigenschaft "Direction" auf "FindReplaceDirection.Backward", um die Suchen-und-Ersetzen-Funktion zu erhalten
    // Operation, um am Ende des Bereichs zu beginnen und zum Anfang zurückzukehren.
    // Setzen Sie die Eigenschaft "Direction" auf "FindReplaceDirection.Forward", um die Suchen-und-Ersetzen-Funktion zu erhalten
    // Operation, um am Anfang des Bereichs zu beginnen und bis zum Ende zu durchlaufen.
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
/// Zeichnet alle Übereinstimmungen auf, die während einer Suchen-und-Ersetzen-Operation auftreten, und zwar in der Reihenfolge, in der sie stattfinden.
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

### Siehe auch

* enum [FindReplaceDirection](../../findreplacedirection/)
* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Montage [Aspose.Words](../../../)
