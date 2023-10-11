---
title: FindReplaceOptions.IgnoreInserted
second_title: Aspose.Words für .NET-API-Referenz
description: FindReplaceOptions eigendom. Ruft einen booleschen Wert ab oder legt ihn fest der angibt ob Text in Einfügungsrevisionen ignoriert werden soll. Der Standardwert istFALSCH .
type: docs
weight: 100
url: /de/net/aspose.words.replacing/findreplaceoptions/ignoreinserted/
---
## FindReplaceOptions.IgnoreInserted property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Text in Einfügungsrevisionen ignoriert werden soll. Der Standardwert ist`FALSCH` .

```csharp
public bool IgnoreInserted { get; set; }
```

### Beispiele

Zeigt, wie Text in Einfügungsrevisionen während eines Suchen-und-Ersetzen-Vorgangs eingefügt oder ignoriert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Beginnen Sie mit der Verfolgung von Revisionen und fügen Sie einen Absatz ein. Bei diesem Absatz handelt es sich um eine Einfügungsrevision.
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("Hello again!");
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsInsertRevision);

// Wir können ein „FindReplaceOptions“-Objekt verwenden, um den Such- und Ersetzungsprozess zu ändern.
FindReplaceOptions options = new FindReplaceOptions();

// Setzen Sie das Flag „IgnoreInserted“ auf „true“, um das Suchen und Ersetzen zu erhalten
// Operation zum Ignorieren von Absätzen, bei denen es sich um Einfügungsrevisionen handelt.
// Setzen Sie das Flag „IgnoreInserted“ auf „false“, um das Suchen und Ersetzen zu erhalten
// Operation, um auch innerhalb von Einfügungsrevisionen nach Text zu suchen.
options.IgnoreInserted = ignoreTextInsideInsertRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideInsertRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### Siehe auch

* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../findreplaceoptions/)
* Montage [Aspose.Words](../../../)


