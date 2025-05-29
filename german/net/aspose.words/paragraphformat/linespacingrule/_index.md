---
title: ParagraphFormat.LineSpacingRule
linktitle: LineSpacingRule
articleTitle: LineSpacingRule
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „PargraphFormat LineSpacingRule“, um den Zeilenabstand von Absätzen einfach anzupassen und so die Lesbarkeit und den Stil Ihrer Dokumente zu verbessern.
type: docs
weight: 200
url: /de/net/aspose.words/paragraphformat/linespacingrule/
---
## ParagraphFormat.LineSpacingRule property

Ruft den Zeilenabstand für den Absatz ab oder legt ihn fest.

```csharp
public LineSpacingRule LineSpacingRule { get; set; }
```

## Beispiele

Zeigt, wie mit Zeilenabständen gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Unten sind drei Zeilenabstandsregeln aufgeführt, die wir mithilfe der
// Eigenschaft „LineSpacingRule“ des Absatzes zum Konfigurieren des Abstands zwischen Absätzen.
// 1 – Legen Sie einen Mindestabstand fest.
// Dadurch werden Textzeilen beliebiger Größe vertikal aufgefüllt.
// das ist zu klein, um die minimale Zeilenhöhe einzuhalten.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.AtLeast;
builder.ParagraphFormat.LineSpacing = 20;

builder.Writeln("Minimum line spacing of 20.");
builder.Writeln("Minimum line spacing of 20.");

// 2 - Genauen Abstand festlegen.
// Wenn Sie für den Abstand zu große Schriftgrößen verwenden, wird der Text abgeschnitten.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Exactly;
builder.ParagraphFormat.LineSpacing = 5;

builder.Writeln("Line spacing of exactly 5.");
builder.Writeln("Line spacing of exactly 5.");

// 3 – Legen Sie den Abstand als Vielfaches des Standardzeilenabstands fest, der standardmäßig 12 Punkte beträgt.
// Diese Art der Abstände werden an verschiedene Schriftgrößen angepasst.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Multiple;
builder.ParagraphFormat.LineSpacing = 18;

builder.Writeln("Line spacing of 1.5 default lines.");
builder.Writeln("Line spacing of 1.5 default lines.");

doc.Save(ArtifactsDir + "ParagraphFormat.LineSpacing.docx");
```

### Siehe auch

* enum [LineSpacingRule](../../linespacingrule/)
* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
