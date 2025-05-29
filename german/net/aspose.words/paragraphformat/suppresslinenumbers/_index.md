---
title: ParagraphFormat.SuppressLineNumbers
linktitle: SuppressLineNumbers
articleTitle: SuppressLineNumbers
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der Eigenschaft „PargraphFormat SuppressLineNumbers“ die Zeilennummerierung für Absätze anpassen und so die Übersichtlichkeit und Organisation des Dokuments verbessern können.
type: docs
weight: 390
url: /de/net/aspose.words/paragraphformat/suppresslinenumbers/
---
## ParagraphFormat.SuppressLineNumbers property

Gibt an, ob die Zeilen des aktuellen Absatzes von der Zeilennummerierung ausgenommen werden sollen, die im übergeordneten Abschnitt angewendet wird.

```csharp
public bool SuppressLineNumbers { get; set; }
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

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
