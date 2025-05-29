---
title: FindReplaceOptions.IgnoreDeleted
linktitle: IgnoreDeleted
articleTitle: IgnoreDeleted
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „IgnoreDeleted“ von FindReplaceOptions und steuern Sie die Textsichtbarkeit in gelöschten Revisionen mit einem einfachen Booleschen Schalter. Verbessern Sie Ihr Bearbeitungserlebnis!
type: docs
weight: 60
url: /de/net/aspose.words.replacing/findreplaceoptions/ignoredeleted/
---
## FindReplaceOptions.IgnoreDeleted property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Text in gelöschten Revisionen ignoriert werden soll. Der Standardwert ist`FALSCH` .

```csharp
public bool IgnoreDeleted { get; set; }
```

## Beispiele

Zeigt, wie Text beim Löschen von Revisionen während eines Suchen-und-Ersetzen-Vorgangs eingeschlossen oder ignoriert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Beginnen Sie mit der Revisionsverfolgung und entfernen Sie den zweiten Absatz, wodurch eine gelöschte Revision erstellt wird.
// Dieser Absatz bleibt im Dokument bestehen, bis wir die Löschrevision akzeptieren.
doc.StartTrackRevisions("John Doe", DateTime.Now);
doc.FirstSection.Body.Paragraphs[1].Remove();
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsDeleteRevision);

// Wir können ein „FindReplaceOptions“-Objekt verwenden, um den Such- und Ersetzungsprozess zu ändern.
FindReplaceOptions options = new FindReplaceOptions();

// Setzen Sie das Flag "IgnoreDeleted" auf "true", um die Funktion "Suchen und Ersetzen" zu erhalten.
// Vorgang zum Ignorieren von Absätzen, bei denen es sich um Löschrevisionen handelt.
// Setzen Sie das Flag "IgnoreDeleted" auf "false", um die Funktion "Suchen und Ersetzen" zu erhalten.
// Vorgang, um auch in gelöschten Revisionen nach Text zu suchen.
options.IgnoreDeleted = ignoreTextInsideDeleteRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideDeleteRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### Siehe auch

* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Montage [Aspose.Words](../../../)
