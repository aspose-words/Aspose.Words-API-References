---
title: FindReplaceOptions.UseLegacyOrder
second_title: Aspose.Words för .NET API Referens
description: FindReplaceOptions fast egendom. True indikerar att en textsökning utförs sekventiellt uppifrån och ned med tanke på textrutorna. Standardvärdet ärfalsk .
type: docs
weight: 170
url: /sv/net/aspose.words.replacing/findreplaceoptions/uselegacyorder/
---
## FindReplaceOptions.UseLegacyOrder property

True indikerar att en textsökning utförs sekventiellt uppifrån och ned med tanke på textrutorna. Standardvärdet är`falsk` .

```csharp
public bool UseLegacyOrder { get; set; }
```

### Exempel

Visar hur du ändrar sökordningen för noder när du utför en sök-och-ersätt textoperation.

```csharp
public void UseLegacyOrder(bool useLegacyOrder)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Infoga tre körningar som vi kan söka efter med hjälp av ett regexmönster.
    // Placera en av dessa körningar i en textruta.
    builder.Writeln("[tag 1]");
    Shape textBox = builder.InsertShape(ShapeType.TextBox, 100, 50);
    builder.Writeln("[tag 2]");
    builder.MoveTo(textBox.FirstParagraph);
    builder.Write("[tag 3]");

    // Vi kan använda ett "FindReplaceOptions"-objekt för att ändra sök-och-ersätt-processen.
    FindReplaceOptions options = new FindReplaceOptions();

    // Tilldela en anpassad återuppringning till egenskapen "ReplacingCallback".
    TextReplacementTracker callback = new TextReplacementTracker();
    options.ReplacingCallback = callback;

    // Om vi ställer in egenskapen "UseLegacyOrder" till "true",
    // hitta-och-ersätt operation kommer att gå igenom alla körningar utanför en textruta
    // innan du går igenom dem i en textruta.
    // Om vi ställer in egenskapen "UseLegacyOrder" till "false", kan
    // hitta-och-ersätt operation kommer att gå över alla körningar i ett intervall i sekventiell ordning.
    options.UseLegacyOrder = useLegacyOrder;

    doc.Range.Replace(new Regex(@"\[tag \d*\]"), "", options);

    Assert.AreEqual(useLegacyOrder ?
        new List<string> { "[tag 1]", "[tag 3]", "[tag 2]" } :
        new List<string> { "[tag 1]", "[tag 2]", "[tag 3]" }, callback.Matches);
}

/// <summary>
/// Registrerar ordningen för alla matchningar som inträffar under en sök-och-ersätt-operation.
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

### Se även

* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../findreplaceoptions/)
* hopsättning [Aspose.Words](../../../)


