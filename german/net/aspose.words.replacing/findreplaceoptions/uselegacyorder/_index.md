---
title: FindReplaceOptions.UseLegacyOrder
second_title: Aspose.Words für .NET-API-Referenz
description: FindReplaceOptions eigendom. True gibt an dass eine Textsuche sequentiell von oben nach unten unter Berücksichtigung der Textfelder durchgeführt wird. Der Standardwert ist false.
type: docs
weight: 150
url: /de/net/aspose.words.replacing/findreplaceoptions/uselegacyorder/
---
## FindReplaceOptions.UseLegacyOrder property

True gibt an, dass eine Textsuche sequentiell von oben nach unten unter Berücksichtigung der Textfelder durchgeführt wird. Der Standardwert ist false.

```csharp
public bool UseLegacyOrder { get; set; }
```

### Beispiele

Zeigt, wie die Suchreihenfolge von Knoten geändert wird, wenn eine Textoperation zum Suchen und Ersetzen ausgeführt wird.

```csharp
[TestCase(true)] // ExSkip
[TestCase(false)] // ExSkip
public void UseLegacyOrder(bool useLegacyOrder)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Füge drei Läufe ein, nach denen wir mit einem Regex-Muster suchen können.
    // Platzieren Sie einen dieser Läufe in einem Textfeld.
    builder.Writeln("[tag 1]");
    Shape textBox = builder.InsertShape(ShapeType.TextBox, 100, 50);
    builder.Writeln("[tag 2]");
    builder.MoveTo(textBox.FirstParagraph);
    builder.Write("[tag 3]");

    // Wir können ein "FindReplaceOptions"-Objekt verwenden, um den Suchen-und-Ersetzen-Prozess zu ändern.
    FindReplaceOptions options = new FindReplaceOptions();

    // Weisen Sie der Eigenschaft "ReplacingCallback" einen benutzerdefinierten Rückruf zu.
    TextReplacementTracker callback = new TextReplacementTracker();
    options.ReplacingCallback = callback;

    // Wenn wir die Eigenschaft "UseLegacyOrder" auf "true" setzen, wird die
    // Suchen-und-Ersetzen-Vorgang durchläuft alle Läufe außerhalb eines Textfelds
    // bevor Sie die in einem Textfeld durchgehen.
    // Wenn wir die Eigenschaft "UseLegacyOrder" auf "false" setzen, wird die
    // Suchen-und-Ersetzen-Operation durchläuft alle Läufe in einem Bereich in sequentieller Reihenfolge.
    options.UseLegacyOrder = useLegacyOrder;

    doc.Range.Replace(new Regex(@"\[tag \d*\]"), "", options);

    Assert.AreEqual(useLegacyOrder ?
        new List<string> { "[tag 1]", "[tag 3]", "[tag 2]" } :
        new List<string> { "[tag 1]", "[tag 2]", "[tag 3]" }, callback.Matches);
}

/// <summary>
/// Zeichnet die Reihenfolge aller Übereinstimmungen auf, die während einer Suchen-und-Ersetzen-Operation auftreten.
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

### Siehe auch

* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../findreplaceoptions/)
* Montage [Aspose.Words](../../../)


