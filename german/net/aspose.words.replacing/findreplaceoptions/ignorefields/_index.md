---
title: FindReplaceOptions.IgnoreFields
linktitle: IgnoreFields
articleTitle: IgnoreFields
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FindReplaceOptions IgnoreFields“, um Text in Feldern einfach zu verwalten. Steuern Sie, wann Inhalte ignoriert werden sollen, um eine effiziente Suche zu ermöglichen!
type: docs
weight: 80
url: /de/net/aspose.words.replacing/findreplaceoptions/ignorefields/
---
## FindReplaceOptions.IgnoreFields property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Text in Feldern ignoriert werden soll. Der Standardwert ist`FALSCH` .

```csharp
public bool IgnoreFields { get; set; }
```

## Bemerkungen

Diese Option betrifft das gesamte Feld (alle Knoten zwischen FieldStart UndFieldEnd).

Um nur Feldcodes zu ignorieren, verwenden Sie bitte die entsprechende Option[`IgnoreFieldCodes`](../ignorefieldcodes/).

## Beispiele

Zeigt, wie Text in Feldern ignoriert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertField("QUOTE", "Hello again!");

// Wir können ein „FindReplaceOptions“-Objekt verwenden, um den Suchen-und-Ersetzen-Prozess zu ändern.
FindReplaceOptions options = new FindReplaceOptions();

// Setzen Sie das Flag "IgnoreFields" auf "true", um die Suchen-und-Ersetzen-Funktion zu erhalten
// Operation zum Ignorieren von Text in Feldern.
// Setzen Sie das Flag "IgnoreFields" auf "false", um die Suchen-und-Ersetzen-Funktion zu erhalten
// Operation, um auch innerhalb von Feldern nach Text zu suchen.
options.IgnoreFields = ignoreTextInsideFields;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideFields
        ? "Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015"
        : "Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015", doc.GetText().Trim());
```

### Siehe auch

* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Montage [Aspose.Words](../../../)
