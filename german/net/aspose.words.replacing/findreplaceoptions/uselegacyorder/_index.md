---
title: FindReplaceOptions.UseLegacyOrder
linktitle: UseLegacyOrder
articleTitle: UseLegacyOrder
second_title: Aspose.Words für .NET
description: Entdecken Sie die UseLegacyOrder-Eigenschaft in FindReplaceOptions. Aktivieren Sie sequentielle Textsuchen für höhere Genauigkeit. Standardmäßig ist „false“ eingestellt. Optimieren Sie Ihre Textverarbeitung!
type: docs
weight: 180
url: /de/net/aspose.words.replacing/findreplaceoptions/uselegacyorder/
---
## FindReplaceOptions.UseLegacyOrder property

True gibt an, dass eine Textsuche sequenziell von oben nach unten unter Berücksichtigung der Textfelder durchgeführt wird. Der Standardwert ist`FALSCH` .

```csharp
public bool UseLegacyOrder { get; set; }
```

## Beispiele

Zeigt, wie die Suchreihenfolge von Knoten beim Ausführen einer Textsuch- und -ersetzungsoperation geändert wird.

```csharp
public void UseLegacyOrder(bool useLegacyOrder)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Fügen Sie drei Läufe ein, nach denen wir mithilfe eines Regex-Musters suchen können.
    // Platzieren Sie einen dieser Läufe in einem Textfeld.
    builder.Writeln("[tag 1]");
    Shape textBox = builder.InsertShape(ShapeType.TextBox, 100, 50);
    builder.Writeln("[tag 2]");
    builder.MoveTo(textBox.FirstParagraph);
    builder.Write("[tag 3]");

    // Wir können ein „FindReplaceOptions“-Objekt verwenden, um den Suchen-und-Ersetzen-Prozess zu ändern.
    FindReplaceOptions options = new FindReplaceOptions();

    // Weisen Sie der Eigenschaft „ReplacingCallback“ einen benutzerdefinierten Rückruf zu.
    TextReplacementTracker callback = new TextReplacementTracker();
    options.ReplacingCallback = callback;

    // Wenn wir die Eigenschaft "UseLegacyOrder" auf "true" setzen,
    // Die Such- und Ersetzungsoperation durchläuft alle Läufe außerhalb eines Textfelds
    // bevor Sie die in einem Textfeld durchgehen.
    // Wenn wir die Eigenschaft "UseLegacyOrder" auf "false" setzen,
    // Die Such- und Ersetzungsoperation durchläuft alle Läufe in einem Bereich in sequenzieller Reihenfolge.
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
* namensraum [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Montage [Aspose.Words](../../../)
