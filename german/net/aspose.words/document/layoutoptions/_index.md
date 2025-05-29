---
title: Document.LayoutOptions
linktitle: LayoutOptions
articleTitle: LayoutOptions
second_title: Aspose.Words für .NET
description: Nutzen Sie die Eigenschaft „Document LayoutOptions“, um das Layout Ihres Dokuments effektiv zu steuern. Schalten Sie flexible Gestaltungsmöglichkeiten für eine optimale Präsentation frei.
type: docs
weight: 260
url: /de/net/aspose.words/document/layoutoptions/
---
## Document.LayoutOptions property

Erhält eine[`LayoutOptions`](../../../aspose.words.layout/layoutoptions/) Objekt, das Optionen zur Steuerung des Layoutprozesses dieses Dokuments darstellt.

```csharp
public LayoutOptions LayoutOptions { get; }
```

## Beispiele

Zeigt, wie Text in einem gerenderten Ausgabedokument ausgeblendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Versteckten Text einfügen und dann angeben, ob er aus einem gerenderten Dokument weggelassen werden soll.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

Zeigt, wie Absatzmarken in einem gerenderten Ausgabedokument angezeigt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Fügen Sie einige Absätze hinzu und aktivieren Sie dann Absatzmarken, um die Enden der Absätze anzuzeigen
// mit einem Absatzsymbol (¶), wenn wir das Dokument rendern.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

Zeigt, wie das Erscheinungsbild von Revisionen in einem gerenderten Ausgabedokument geändert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie eine Revision ein und ändern Sie dann die Farbe aller Revisionen in Grün.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Entfernen Sie den Balken, der links neben jeder überarbeiteten Zeile erscheint.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### Siehe auch

* class [LayoutOptions](../../../aspose.words.layout/layoutoptions/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
