---
title: ParagraphFormat.LineSpacing
linktitle: LineSpacing
articleTitle: LineSpacing
second_title: Aspose.Words für .NET
description: ParagraphFormat LineSpacing eigendom. Ruft den Zeilenabstand in Punkt für den Absatz ab oder legt diesen fest in C#.
type: docs
weight: 190
url: /de/net/aspose.words/paragraphformat/linespacing/
---
## ParagraphFormat.LineSpacing property

Ruft den Zeilenabstand (in Punkt) für den Absatz ab oder legt diesen fest.

```csharp
public double LineSpacing { get; set; }
```

## Bemerkungen

Wann[`LineSpacingRule`](../linespacingrule/) Die Eigenschaft ist auf festgelegtAtLeast , der Zeilenabstand kann größer oder gleich, sein, jedoch niemals kleiner als der angegebene`LineSpacing` Wert.

Wann[`LineSpacingRule`](../linespacingrule/) Die Eigenschaft ist auf festgelegtExactly , der Zeilenabstand ändert sich nie von zum angegebenen`LineSpacing` Wert, auch wenn innerhalb des Absatzes eine größere Schriftart verwendet wird.

## Beispiele

Zeigt, wie mit Zeilenabständen gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nachfolgend finden Sie drei Zeilenabstandsregeln, die wir mithilfe von definieren können
// „LineSpacingRule“-Eigenschaft des Absatzes, um den Abstand zwischen Absätzen zu konfigurieren.
// 1 – Legen Sie einen Mindestabstand fest.
// Dadurch werden Textzeilen beliebiger Größe vertikal aufgefüllt
// das ist zu klein, um die minimale Zeilenhöhe einzuhalten.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.AtLeast;
builder.ParagraphFormat.LineSpacing = 20;

builder.Writeln("Minimum line spacing of 20.");
builder.Writeln("Minimum line spacing of 20.");

// 2 – Genauen Abstand festlegen.
// Wenn Sie für den Abstand zu große Schriftgrößen verwenden, wird der Text abgeschnitten.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Exactly;
builder.ParagraphFormat.LineSpacing = 5;

builder.Writeln("Line spacing of exactly 5.");
builder.Writeln("Line spacing of exactly 5.");

// 3 – Legen Sie den Abstand als Vielfaches des Standardzeilenabstands fest, der standardmäßig 12 Punkte beträgt.
// Diese Art von Abstand passt sich an unterschiedliche Schriftgrößen an.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Multiple;
builder.ParagraphFormat.LineSpacing = 18;

builder.Writeln("Line spacing of 1.5 default lines.");
builder.Writeln("Line spacing of 1.5 default lines.");

doc.Save(ArtifactsDir + "ParagraphFormat.LineSpacing.docx");
```

### Siehe auch

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
