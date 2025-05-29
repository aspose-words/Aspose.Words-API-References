---
title: LineSpacingRule Enum
linktitle: LineSpacingRule
articleTitle: LineSpacingRule
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.LineSpacingRule-Aufzählung für anpassbaren Absatzzeilenabstand. Verbessern Sie die Dokumentformatierung mit präziser Steuerung und verbesserter Lesbarkeit.
type: docs
weight: 3890
url: /de/net/aspose.words/linespacingrule/
---
## LineSpacingRule enumeration

Gibt den Zeilenabstand für einen Absatz an.

```csharp
public enum LineSpacingRule
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| AtLeast | `0` | Der Zeilenabstand kann größer oder gleich, aber nie kleiner als der in der[`LineSpacing`](../paragraphformat/linespacing/) Eigenschaft. |
| Exactly | `1` | Der Zeilenabstand ändert sich nie von dem in angegebenen Wert.[`LineSpacing`](../paragraphformat/linespacing/) Eigenschaft, , auch wenn innerhalb des Absatzes eine größere Schriftart verwendet wird. |
| Multiple | `2` | Der Zeilenabstand wird in der[`LineSpacing`](../paragraphformat/linespacing/) Eigenschaft als Anzahl der Zeilen. Eine Zeile entspricht 12 Punkten. |

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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
