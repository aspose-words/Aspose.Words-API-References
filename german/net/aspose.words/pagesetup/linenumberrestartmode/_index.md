---
title: PageSetup.LineNumberRestartMode
second_title: Aspose.Words für .NET-API-Referenz
description: PageSetup eigendom. Ruft ab oder legt fest wie die Zeilennummerierung ausgeführt wird d. h. ob sie am Anfang einer neuen Seite oder eines neuen Abschnitts neu beginnt oder fortlaufend ausgeführt wird.
type: docs
weight: 230
url: /de/net/aspose.words/pagesetup/linenumberrestartmode/
---
## PageSetup.LineNumberRestartMode property

Ruft ab oder legt fest, wie die Zeilennummerierung ausgeführt wird, d. h. ob sie am Anfang einer neuen Seite oder eines neuen Abschnitts neu beginnt oder fortlaufend ausgeführt wird.

```csharp
public LineNumberRestartMode LineNumberRestartMode { get; set; }
```

### Beispiele

Zeigt, wie die Zeilennummerierung für einen Abschnitt aktiviert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wir können das PageSetup-Objekt des Abschnitts verwenden, um Zahlen links von den Textzeilen des Abschnitts anzuzeigen.
// Dies ist das gleiche Verhalten wie bei einem Listenobjekt.
// aber es deckt den gesamten Abschnitt ab und verändert den Text in keiner Weise.
// Unser Abschnitt startet die Nummerierung auf jeder neuen Seite von 1 an und zeigt die Nummer an,
// wenn es ein Vielfaches von 3 ist, bei 50pt links von der Linie.
PageSetup pageSetup = builder.PageSetup;
pageSetup.LineStartingNumber = 1;
pageSetup.LineNumberCountBy = 3;
pageSetup.LineNumberRestartMode = LineNumberRestartMode.RestartPage;
pageSetup.LineNumberDistanceFromText = 50.0d;

for (int i = 1; i <= 25; i++)
    builder.Writeln($"Line {i}.");

// Der Zeilenzähler überspringt jeden Absatz, bei dem das Flag „SuppressLineNumbers“ auf „true“ gesetzt ist.
// Dieser Absatz befindet sich in der 15. Zeile, was ein Vielfaches von 3 ist, und würde daher normalerweise eine Zeilennummer anzeigen.
// Der Zeilenzähler des Abschnitts ignoriert diese Zeile ebenfalls und behandelt die nächste Zeile als 15.
// und die Zählung von diesem Punkt an fortsetzen.
doc.FirstSection.Body.Paragraphs[14].ParagraphFormat.SuppressLineNumbers = true;

doc.Save(ArtifactsDir + "PageSetup.LineNumbers.docx");
```

### Siehe auch

* enum [LineNumberRestartMode](../../linenumberrestartmode/)
* class [PageSetup](../)
* namensraum [Aspose.Words](../../pagesetup/)
* Montage [Aspose.Words](../../../)


