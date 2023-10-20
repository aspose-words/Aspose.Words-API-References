---
title: FindReplaceOptions.IgnoreDeleted
linktitle: IgnoreDeleted
articleTitle: IgnoreDeleted
second_title: Aspose.Words für .NET
description: FindReplaceOptions IgnoreDeleted eigendom. Ruft einen booleschen Wert ab oder legt diesen fest der angibt ob Text in Löschrevisionen ignoriert werden soll. Der Standardwert istFALSCH  in C#.
type: docs
weight: 60
url: /de/net/aspose.words.replacing/findreplaceoptions/ignoredeleted/
---
## FindReplaceOptions.IgnoreDeleted property

Ruft einen booleschen Wert ab oder legt diesen fest, der angibt, ob Text in Löschrevisionen ignoriert werden soll. Der Standardwert ist`FALSCH` .

```csharp
public bool IgnoreDeleted { get; set; }
```

## Beispiele

Zeigt, wie Text in Löschrevisionen während eines Suchen-und-Ersetzen-Vorgangs eingefügt oder ignoriert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Beginnen Sie mit der Verfolgung von Revisionen und entfernen Sie den zweiten Absatz, wodurch eine Löschrevision erstellt wird.
// Dieser Absatz bleibt im Dokument bestehen, bis wir die Löschrevision akzeptieren.
doc.StartTrackRevisions("John Doe", DateTime.Now);
doc.FirstSection.Body.Paragraphs[1].Remove();
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsDeleteRevision);

// Wir können ein „FindReplaceOptions“-Objekt verwenden, um den Such- und Ersetzungsprozess zu ändern.
FindReplaceOptions options = new FindReplaceOptions();

// Setzen Sie das Flag „IgnoreDeleted“ auf „true“, um das Suchen und Ersetzen zu erhalten
// Operation zum Ignorieren von Absätzen, bei denen es sich um Löschrevisionen handelt.
// Setzen Sie das Flag „IgnoreDeleted“ auf „false“, um das Suchen und Ersetzen zu erhalten
// Operation, um auch innerhalb von Löschrevisionen nach Text zu suchen.
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
