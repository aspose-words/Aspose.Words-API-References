---
title: PageSetup.LineNumberRestartMode
linktitle: LineNumberRestartMode
articleTitle: LineNumberRestartMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „PageSetup LineNumberRestartMode“ zur Steuerung der Zeilennummerierung – wählen Sie zwischen Neustart auf neuen Seiten oder fortlaufender Nummerierung für nahtlose Dokumente.
type: docs
weight: 230
url: /de/net/aspose.words/pagesetup/linenumberrestartmode/
---
## PageSetup.LineNumberRestartMode property

Ruft die Art und Weise ab, in der die Zeilennummerierung ausgeführt wird, d. h., ob sie am Anfang einer neuen Seite oder eines neuen Abschnitts neu beginnt oder kontinuierlich ausgeführt wird.

```csharp
public LineNumberRestartMode LineNumberRestartMode { get; set; }
```

## Beispiele

Zeigt, wie die Zeilennummerierung für einen Abschnitt aktiviert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wir können das PageSetup-Objekt des Abschnitts verwenden, um Zahlen links von den Textzeilen des Abschnitts anzuzeigen.
// Dies ist das gleiche Verhalten wie bei einem List-Objekt.
// aber es deckt den gesamten Abschnitt ab und ändert den Text in keiner Weise.
// Unser Abschnitt beginnt die Nummerierung auf jeder neuen Seite wieder bei 1 und zeigt die Nummer an,
// wenn es ein Vielfaches von 3 ist, 50pt links von der Zeile.
PageSetup pageSetup = builder.PageSetup;
pageSetup.LineStartingNumber = 1;
pageSetup.LineNumberCountBy = 3;
pageSetup.LineNumberRestartMode = LineNumberRestartMode.RestartPage;
pageSetup.LineNumberDistanceFromText = 50.0d;

for (int i = 1; i <= 25; i++)
    builder.Writeln($"Line {i}.");

// Der Zeilenzähler überspringt alle Absätze, bei denen das Flag „SuppressLineNumbers“ auf „true“ gesetzt ist.
// Dieser Absatz steht in der 15. Zeile, die ein Vielfaches von 3 ist, und würde daher normalerweise eine Zeilennummer anzeigen.
// Der Zeilenzähler des Abschnitts ignoriert diese Zeile ebenfalls und behandelt die nächste Zeile als die 15.
// und von diesem Punkt an weiter zählen.
doc.FirstSection.Body.Paragraphs[14].ParagraphFormat.SuppressLineNumbers = true;

doc.Save(ArtifactsDir + "PageSetup.LineNumbers.docx");
```

### Siehe auch

* enum [LineNumberRestartMode](../../linenumberrestartmode/)
* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
