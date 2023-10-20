---
title: LineNumberRestartMode Enum
linktitle: LineNumberRestartMode
articleTitle: LineNumberRestartMode
second_title: Aspose.Words für .NET
description: Aspose.Words.LineNumberRestartMode opsomming. Legt fest wann die automatische Zeilennummerierung neu startet in C#.
type: docs
weight: 3430
url: /de/net/aspose.words/linenumberrestartmode/
---
## LineNumberRestartMode enumeration

Legt fest, wann die automatische Zeilennummerierung neu startet.

```csharp
public enum LineNumberRestartMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| RestartPage | `0` | Die Zeilennummerierung beginnt am Anfang jeder Seite neu. |
| RestartSection | `1` | Die Zeilennummerierung beginnt wieder am Abschnittsanfang. |
| Continuous | `2` | Zeilennummerierung fortlaufend vom vorherigen Abschnitt. |

## Beispiele

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

* class [PageSetup](../pagesetup/)
* property [LineNumberRestartMode](../pagesetup/linenumberrestartmode/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
