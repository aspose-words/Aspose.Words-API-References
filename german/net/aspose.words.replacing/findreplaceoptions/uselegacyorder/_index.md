---
title: FindReplaceOptions.UseLegacyOrder
linktitle: UseLegacyOrder
articleTitle: UseLegacyOrder
second_title: Aspose.Words für .NET
description: FindReplaceOptions UseLegacyOrder eigendom. True gibt an dass eine Textsuche der Reihe nach von oben nach unten unter Berücksichtigung der Textfelder durchgeführt wird. Der Standardwert istFALSCH  in C#.
type: docs
weight: 170
url: /de/net/aspose.words.replacing/findreplaceoptions/uselegacyorder/
---
## FindReplaceOptions.UseLegacyOrder property

True gibt an, dass eine Textsuche der Reihe nach von oben nach unten unter Berücksichtigung der Textfelder durchgeführt wird. Der Standardwert ist`FALSCH` .

```csharp
public bool UseLegacyOrder { get; set; }
```

## Beispiele

Zeigt, wie die Suchreihenfolge von Knoten geändert wird, wenn eine Textoperation zum Suchen und Ersetzen ausgeführt wird.

```csharp
public void UseLegacyOrder(bool useLegacyOrder)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Drei Läufe einfügen, nach denen wir mithilfe eines Regex-Musters suchen können.
    // Platziere einen dieser Läufe in einem Textfeld.
    builder.Writeln("[tag 1]");
    Shape textBox = builder.InsertShape(ShapeType.TextBox, 100, 50);
    builder.Writeln("[tag 2]");
    builder.MoveTo(textBox.FirstParagraph);
    builder.Write("[tag 3]");

    // Wir können ein „FindReplaceOptions“-Objekt verwenden, um den Such- und Ersetzungsprozess zu ändern.
    FindReplaceOptions options = new FindReplaceOptions();

    // Weisen Sie der Eigenschaft „ReplacingCallback“ einen benutzerdefinierten Rückruf zu.
    TextReplacementTracker callback = new TextReplacementTracker();
    options.ReplacingCallback = callback;

    // Wenn wir die Eigenschaft „UseLegacyOrder“ auf „true“ setzen, wird die
    // Der Such- und Ersetzungsvorgang durchläuft alle Läufe außerhalb eines Textfelds
    // bevor Sie die in einem Textfeld durchgehen.
    // Wenn wir die Eigenschaft „UseLegacyOrder“ auf „false“ setzen, wird die
    // Der Such- und Ersetzungsvorgang durchläuft alle Läufe in einem Bereich in sequentieller Reihenfolge.
    options.UseLegacyOrder = useLegacyOrder;

    doc.Range.Replace(new Regex(@"\[tag \d*\]"), "", options);

    Assert.AreEqual(useLegacyOrder ?
        new List<string> { "[tag 1]", "[tag 3]", "[tag 2]" } :
        new List<string> { "[tag 1]", "[tag 2]", "[tag 3]" }, callback.Matches);
}

/// <summary>
/// Zeichnet die Reihenfolge aller Übereinstimmungen auf, die während eines Such- und Ersetzungsvorgangs auftreten.
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
* namensraum [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Montage [Aspose.Words](../../../)
