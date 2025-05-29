---
title: PageSetup.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words für .NET
description: Entdecken Sie die PageSetup Bidi-Eigenschaft für nahtlose bidirektionale Textformatierung. Verbessern Sie Ihre Dokumente mit komplexer Skriptunterstützung für bessere Lesbarkeit!
type: docs
weight: 10
url: /de/net/aspose.words/pagesetup/bidi/
---
## PageSetup.Bidi property

Gibt an, dass dieser Abschnitt bidirektionalen Text (komplexe Skripts) enthält.

```csharp
public bool Bidi { get; set; }
```

## Bemerkungen

Wann`WAHR`, die Spalten in diesem Abschnitt sind von rechts nach links angeordnet.

## Beispiele

Zeigt, wie die Reihenfolge der Textspalten in einem Abschnitt festgelegt wird.

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextColumns.SetCount(3);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Write("Column 2.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Write("Column 3.");

// Setzen Sie die Eigenschaft „Bidi“ auf „true“, um die Spalten beginnend auf der rechten Seite der Seite anzuordnen.
// Die Reihenfolge der Spalten entspricht der Richtung des von rechts nach links verlaufenden Textes.
// Setzen Sie die Eigenschaft „Bidi“ auf „false“, um die Spalten beginnend auf der linken Seite der Seite anzuordnen.
// Die Reihenfolge der Spalten entspricht der Richtung des Textes von links nach rechts.
pageSetup.Bidi = reverseColumns;

doc.Save(ArtifactsDir + "PageSetup.Bidi.docx");
```

### Siehe auch

* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
