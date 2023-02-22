---
title: PageSetup.LineNumberDistanceFromText
second_title: Aspose.Words für .NET-API-Referenz
description: PageSetup eigendom. Ruft den Abstand zwischen dem rechten Rand der Zeilennummern und dem linken Rand des Dokuments ab oder legt ihn fest.
type: docs
weight: 220
url: /de/net/aspose.words/pagesetup/linenumberdistancefromtext/
---
## PageSetup.LineNumberDistanceFromText property

Ruft den Abstand zwischen dem rechten Rand der Zeilennummern und dem linken Rand des Dokuments ab oder legt ihn fest.

```csharp
public double LineNumberDistanceFromText { get; set; }
```

### Bemerkungen

Setzen Sie diese Eigenschaft auf Null für den automatischen Abstand zwischen den Zeilennummern und dem Text des Dokuments.

### Beispiele

Zeigt, wie die Zeilennummerierung für einen Abschnitt aktiviert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wir können das PageSetup-Objekt des Abschnitts verwenden, um Zahlen links von den Textzeilen des Abschnitts anzuzeigen.
// Dies ist das gleiche Verhalten wie bei einem List-Objekt,
// aber es deckt den gesamten Abschnitt ab und verändert den Text in keiner Weise.
// Unser Abschnitt beginnt die Nummerierung auf jeder neuen Seite von 1 neu und zeigt die Nummer an,
// wenn es ein Vielfaches von 3 ist, bei 50 pt links von der Zeile.
PageSetup pageSetup = builder.PageSetup;
pageSetup.LineStartingNumber = 1;
pageSetup.LineNumberCountBy = 3;
pageSetup.LineNumberRestartMode = LineNumberRestartMode.RestartPage;
pageSetup.LineNumberDistanceFromText = 50.0d;

for (int i = 1; i <= 25; i++)
    builder.Writeln($"Line {i}.");

// Der Zeilenzähler überspringt jeden Absatz, bei dem das "SuppressLineNumbers"-Flag auf "true" gesetzt ist.
// Dieser Absatz befindet sich in der 15. Zeile, die ein Vielfaches von 3 ist, und würde daher normalerweise eine Zeilennummer anzeigen.
// Der Zeilenzähler des Abschnitts wird diese Zeile ebenfalls ignorieren, die nächste Zeile als die 15. behandeln,
// und die Zählung von diesem Punkt an fortsetzen.
doc.FirstSection.Body.Paragraphs[14].ParagraphFormat.SuppressLineNumbers = true;

doc.Save(ArtifactsDir + "PageSetup.LineNumbers.docx");
```

### Siehe auch

* class [PageSetup](../)
* namensraum [Aspose.Words](../../pagesetup/)
* Montage [Aspose.Words](../../../)


