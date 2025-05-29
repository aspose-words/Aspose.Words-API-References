---
title: FindReplaceOptions.IgnoreInserted
linktitle: IgnoreInserted
articleTitle: IgnoreInserted
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „IgnoreInserted“ von FindReplaceOptions und steuern Sie die Textverarbeitung in Einfügerevisionen mit dieser einfachen booleschen Einstellung. Der Standardwert ist „false“.
type: docs
weight: 100
url: /de/net/aspose.words.replacing/findreplaceoptions/ignoreinserted/
---
## FindReplaceOptions.IgnoreInserted property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Text in eingefügten Revisionen ignoriert werden soll. Der Standardwert ist`FALSCH` .

```csharp
public bool IgnoreInserted { get; set; }
```

## Beispiele

Zeigt, wie Text in eingefügten Revisionen während eines Suchen-und-Ersetzen-Vorgangs eingeschlossen oder ignoriert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Starten Sie die Revisionsverfolgung und fügen Sie einen Absatz ein. Dieser Absatz wird als eingefügte Revision verwendet.
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("Hello again!");
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsInsertRevision);

// Wir können ein „FindReplaceOptions“-Objekt verwenden, um den Suchen-und-Ersetzen-Prozess zu ändern.
FindReplaceOptions options = new FindReplaceOptions();

// Setzen Sie das Flag "IgnoreInserted" auf "true", um die Suchen-und-Ersetzen-Funktion zu erhalten
// Vorgang zum Ignorieren von Absätzen, bei denen es sich um eingefügte Revisionen handelt.
// Setzen Sie das Flag "IgnoreInserted" auf "false", um die Suchen-und-Ersetzen-Funktion zu erhalten
// Vorgang, um auch in eingefügten Revisionen nach Text zu suchen.
options.IgnoreInserted = ignoreTextInsideInsertRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideInsertRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### Siehe auch

* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Montage [Aspose.Words](../../../)
