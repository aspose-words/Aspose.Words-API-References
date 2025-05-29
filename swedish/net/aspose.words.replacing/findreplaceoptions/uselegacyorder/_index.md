---
title: FindReplaceOptions.UseLegacyOrder
linktitle: UseLegacyOrder
articleTitle: UseLegacyOrder
second_title: Aspose.Words för .NET
description: Upptäck egenskapen UseLegacyOrder i FindReplaceOptions. Aktivera sekventiella textsökningar för bättre noggrannhet. Standardvärdet är falskt. Optimera din textbehandling!
type: docs
weight: 180
url: /sv/net/aspose.words.replacing/findreplaceoptions/uselegacyorder/
---
## FindReplaceOptions.UseLegacyOrder property

True indikerar att en textsökning utförs sekventiellt uppifrån och ned med hänsyn till textrutorna. Standardvärdet är`falsk` .

```csharp
public bool UseLegacyOrder { get; set; }
```

## Exempel

Visar hur man ändrar sökordningen för noder när man utför en sök-och-ersätt-textåtgärd.

```csharp
public void UseLegacyOrder(bool useLegacyOrder)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Infoga tre körningar som vi kan söka efter med hjälp av ett regex-mönster.
    // Placera en av dessa körningar i en textruta.
    builder.Writeln("[tag 1]");
    Shape textBox = builder.InsertShape(ShapeType.TextBox, 100, 50);
    builder.Writeln("[tag 2]");
    builder.MoveTo(textBox.FirstParagraph);
    builder.Write("[tag 3]");

    // Vi kan använda ett "FindReplaceOptions"-objekt för att modifiera sök-och-ersätt-processen.
    FindReplaceOptions options = new FindReplaceOptions();

    // Tilldela en anpassad återanropning till egenskapen "ReplacingCallback".
    TextReplacementTracker callback = new TextReplacementTracker();
    options.ReplacingCallback = callback;

    // Om vi ställer in egenskapen "UseLegacyOrder" till "true", så
    // sök-och-ersätt-operationen går igenom alla körningar utanför en textruta
    // innan man går igenom de som finns i en textruta.
    // Om vi ställer in egenskapen "UseLegacyOrder" till "false", så
    // sök-och-ersätt-operationen går igenom alla körningar i ett intervall i sekventiell ordning.
    options.UseLegacyOrder = useLegacyOrder;

    doc.Range.Replace(new Regex(@"\[tag \d*\]"), "", options);

    Assert.AreEqual(useLegacyOrder ?
        new List<string> { "[tag 1]", "[tag 3]", "[tag 2]" } :
        new List<string> { "[tag 1]", "[tag 2]", "[tag 3]" }, callback.Matches);
}

/// <summary>
/// Registrerar ordningen på alla träffar som inträffar under en sök-och-ersätt-operation.
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
* namnutrymme [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../../)
