---
title: TextBox Class
linktitle: TextBox
articleTitle: TextBox
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.TextBox, um die Textanzeige in Formen einfach anzupassen und so die visuelle Attraktivität und Funktionalität Ihres Dokuments zu verbessern.
type: docs
weight: 1730
url: /de/net/aspose.words.drawing/textbox/
---
## TextBox class

Definiert Attribute, die angeben, wie ein Text innerhalb einer Form angezeigt wird.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Formen](https://docs.aspose.com/words/net/working-with-shapes/) Dokumentationsartikel.

```csharp
public class TextBox
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [FitShapeToText](../../aspose.words.drawing/textbox/fitshapetotext/) { get; set; } | Bestimmt, ob Microsoft Word die Form an den Text anpasst. |
| [InternalMarginBottom](../../aspose.words.drawing/textbox/internalmarginbottom/) { get; set; } | Gibt den inneren unteren Rand einer Form in Punkten an. |
| [InternalMarginLeft](../../aspose.words.drawing/textbox/internalmarginleft/) { get; set; } | Gibt den inneren linken Rand einer Form in Punkten an. |
| [InternalMarginRight](../../aspose.words.drawing/textbox/internalmarginright/) { get; set; } | Gibt den inneren rechten Rand einer Form in Punkten an. |
| [InternalMarginTop](../../aspose.words.drawing/textbox/internalmargintop/) { get; set; } | Gibt den inneren oberen Rand einer Form in Punkten an. |
| [LayoutFlow](../../aspose.words.drawing/textbox/layoutflow/) { get; set; } | Bestimmt den Fluss des Textlayouts in einer Form. |
| [Next](../../aspose.words.drawing/textbox/next/) { get; set; } | Gibt zurück oder setzt einen`TextBox` das stellt die nächste`TextBox`in einer Abfolge von Formen. |
| [NoTextRotation](../../aspose.words.drawing/textbox/notextrotation/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, dass der Text des Textfelds nicht gedreht werden soll, wenn die Form gedreht wird. |
| [Parent](../../aspose.words.drawing/textbox/parent/) { get; } | Ruft eine übergeordnete Form für die`TextBox` . |
| [Previous](../../aspose.words.drawing/textbox/previous/) { get; } | Gibt einen`TextBox` das stellt die vorherige`TextBox`in einer Abfolge von Formen. |
| [TextBoxWrapMode](../../aspose.words.drawing/textbox/textboxwrapmode/) { get; set; } | Bestimmt, wie Text innerhalb einer Form umbrochen wird. |
| [VerticalAnchor](../../aspose.words.drawing/textbox/verticalanchor/) { get; set; } | Gibt die vertikale Ausrichtung des Textes innerhalb einer Form an. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [BreakForwardLink](../../aspose.words.drawing/textbox/breakforwardlink/)() | Unterbricht die Verbindung zum nächsten`TextBox` . |
| [IsValidLinkTarget](../../aspose.words.drawing/textbox/isvalidlinktarget/)(*TextBox*) | Bestimmt, ob diese`TextBox` kann mit dem Ziel verknüpft werden`TextBox` . |

## Bemerkungen

Verwenden Sie die[`TextBox`](../shape/textbox/) Eigenschaft, um auf die Texteigenschaften einer Form zuzugreifen. Sie erstellen keine Instanzen der`TextBox` Klasse direkt.

## Beispiele

Zeigt, wie interne Ränder für ein Textfeld festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein weiteres Textfeld mit bestimmten Rändern ein.
Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox = textBoxShape.TextBox;
textBox.InternalMarginTop = 15;
textBox.InternalMarginBottom = 15;
textBox.InternalMarginLeft = 15;
textBox.InternalMarginRight = 15;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text placed according to textbox margins.");

doc.Save(ArtifactsDir + "Shape.TextBoxMargins.docx");
```

Zeigt, wie die Ausrichtung von Text in einem Textfeld festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Verschieben Sie den Dokumentgenerator in das Textfeld und fügen Sie Text hinzu.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Legen Sie die Eigenschaft „LayoutFlow“ fest, um eine Ausrichtung für den Textinhalt dieses Textfelds festzulegen.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

Zeigt, wie Sie die Größe eines Textfelds so anpassen, dass sein Inhalt genau hineinpasst.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Wenden Sie diese Werte auf beide Elemente an, damit die übergeordnete Form passt
// eng um den Textinhalt herum, wobei die von uns festgelegten Abmessungen ignoriert werden.
textBox.FitShapeToText = true;
textBox.TextBoxWrapMode = TextBoxWrapMode.None;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text fit tightly inside textbox.");

doc.Save(ArtifactsDir + "Shape.TextBoxFitShapeToText.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
