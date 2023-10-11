---
title: FindReplaceOptions.IgnoreFields
second_title: Aspose.Words für .NET-API-Referenz
description: FindReplaceOptions eigendom. Ruft einen booleschen Wert ab oder legt ihn fest der angibt ob Text in Feldern ignoriert werden soll. Der Standardwert istFALSCH .
type: docs
weight: 80
url: /de/net/aspose.words.replacing/findreplaceoptions/ignorefields/
---
## FindReplaceOptions.IgnoreFields property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Text in Feldern ignoriert werden soll. Der Standardwert ist`FALSCH` .

```csharp
public bool IgnoreFields { get; set; }
```

### Bemerkungen

Diese Option betrifft das gesamte Feld (alle Knoten zwischen FieldStart UndFieldEnd).

Um nur Feldcodes zu ignorieren, verwenden Sie bitte die entsprechende Option[`IgnoreFieldCodes`](../ignorefieldcodes/).

### Beispiele

Zeigt, wie Text in Feldern ignoriert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertField("QUOTE", "Hello again!");

// Wir können ein „FindReplaceOptions“-Objekt verwenden, um den Such- und Ersetzungsprozess zu ändern.
FindReplaceOptions options = new FindReplaceOptions();

// Setzen Sie das Flag „IgnoreFields“ auf „true“, um das Suchen und Ersetzen zu erhalten
// Operation zum Ignorieren von Text in Feldern.
// Setzen Sie das Flag „IgnoreFields“ auf „false“, um das Suchen und Ersetzen zu erhalten
// Operation, um auch nach Text innerhalb von Feldern zu suchen.
options.IgnoreFields = ignoreTextInsideFields;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideFields
        ? "Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015"
        : "Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015", doc.GetText().Trim());
```

### Siehe auch

* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../findreplaceoptions/)
* Montage [Aspose.Words](../../../)


