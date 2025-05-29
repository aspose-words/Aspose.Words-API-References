---
title: FindReplaceOptions.IgnoreFieldCodes
linktitle: IgnoreFieldCodes
articleTitle: IgnoreFieldCodes
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FindReplaceOptions IgnoreFieldCodes“, um Text in Feldcodes einfach zu verwalten. Steuern Sie die Sichtbarkeit mit einer einfachen booleschen Einstellung!
type: docs
weight: 70
url: /de/net/aspose.words.replacing/findreplaceoptions/ignorefieldcodes/
---
## FindReplaceOptions.IgnoreFieldCodes property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Text in Feldcodes ignoriert werden soll. Der Standardwert ist`FALSCH` .

```csharp
public bool IgnoreFieldCodes { get; set; }
```

## Bemerkungen

Diese Option betrifft nur Feldcodes (sie ignoriert keine Knoten zwischen FieldSeparator UndFieldEnd).

Um das gesamte Feld zu ignorieren, verwenden Sie bitte die entsprechende Option[`IgnoreFields`](../ignorefields/).

## Beispiele

Zeigt, wie Text in Feldcodes ignoriert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("INCLUDETEXT", "Test IT!");

FindReplaceOptions options = new FindReplaceOptions {IgnoreFieldCodes = ignoreFieldCodes};

// Ersetzen Sie „T“ im Dokument und ignorieren Sie dabei den Text im Feldcode.
doc.Range.Replace(new Regex("T"), "*", options);
Console.WriteLine(doc.GetText());

Assert.AreEqual(
    ignoreFieldCodes
        ? "\u0013INCLUDETEXT\u0014*est I*!\u0015"
        : "\u0013INCLUDE*EX*\u0014*est I*!\u0015", doc.GetText().Trim());
```

### Siehe auch

* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Montage [Aspose.Words](../../../)
