---
title: LineNumberRestartMode Enum
linktitle: LineNumberRestartMode
articleTitle: LineNumberRestartMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.LineNumberRestartMode, um das automatische Zurücksetzen der Zeilennummerierung für eine verbesserte Dokumentformatierung und Übersichtlichkeit zu steuern.
type: docs
weight: 3880
url: /de/net/aspose.words/linenumberrestartmode/
---
## LineNumberRestartMode enumeration

Bestimmt, wann die automatische Zeilennummerierung neu gestartet wird.

```csharp
public enum LineNumberRestartMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| RestartPage | `0` | Die Zeilennummerierung beginnt am Anfang jeder Seite neu. |
| RestartSection | `1` | Die Zeilennummerierung beginnt am Abschnittsanfang neu. |
| Continuous | `2` | Die Zeilennummerierung erfolgt fortlaufend aus dem vorherigen Abschnitt. |

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

* class [PageSetup](../pagesetup/)
* property [LineNumberRestartMode](../pagesetup/linenumberrestartmode/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
