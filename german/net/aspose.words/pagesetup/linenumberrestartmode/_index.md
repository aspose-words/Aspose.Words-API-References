---
title: PageSetup.LineNumberRestartMode
second_title: Aspose.Words für .NET-API-Referenz
description: PageSetup eigendom. Ermittelt oder legt fest wie die Zeilennummerierung verläuft d. h. ob sie am Anfang einer neuen Seite oder eines Abschnitts neu beginnt oder fortlaufend läuft.
type: docs
weight: 230
url: /de/net/aspose.words/pagesetup/linenumberrestartmode/
---
## PageSetup.LineNumberRestartMode property

Ermittelt oder legt fest, wie die Zeilennummerierung verläuft, d. h. ob sie am Anfang einer neuen Seite oder eines Abschnitts neu beginnt oder fortlaufend läuft.

```csharp
public LineNumberRestartMode LineNumberRestartMode { get; set; }
```

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

* enum [LineNumberRestartMode](../../linenumberrestartmode/)
* class [PageSetup](../)
* namensraum [Aspose.Words](../../pagesetup/)
* Montage [Aspose.Words](../../../)


