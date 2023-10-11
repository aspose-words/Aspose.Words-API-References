---
title: Class TextBox
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.TextBox klas. Definiert Attribute die angeben wie ein Text innerhalb einer Form angezeigt wird.
type: docs
weight: 1320
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
| [FitShapeToText](../../aspose.words.drawing/textbox/fitshapetotext/) { get; set; } | Legt fest, ob Microsoft Word die Form an den Text anpasst. |
| [InternalMarginBottom](../../aspose.words.drawing/textbox/internalmarginbottom/) { get; set; } | Gibt den inneren unteren Rand in Punkten für eine Form an. |
| [InternalMarginLeft](../../aspose.words.drawing/textbox/internalmarginleft/) { get; set; } | Gibt den inneren linken Rand in Punkten für eine Form an. |
| [InternalMarginRight](../../aspose.words.drawing/textbox/internalmarginright/) { get; set; } | Gibt den inneren rechten Rand in Punkten für eine Form an. |
| [InternalMarginTop](../../aspose.words.drawing/textbox/internalmargintop/) { get; set; } | Gibt den inneren oberen Rand in Punkten für eine Form an. |
| [LayoutFlow](../../aspose.words.drawing/textbox/layoutflow/) { get; set; } | Bestimmt den Fluss des Textlayouts in einer Form. |
| [Next](../../aspose.words.drawing/textbox/next/) { get; set; } | Gibt a zurück oder legt es fest`TextBox` das stellt das nächste dar`TextBox` in einer Folge von Formen. |
| [NoTextRotation](../../aspose.words.drawing/textbox/notextrotation/) { get; set; } | Ruft einen booleschen Wert ab oder legt diesen fest, der angibt, dass sich der Text der TextBox nicht drehen soll, wenn die Form gedreht wird. |
| [Parent](../../aspose.words.drawing/textbox/parent/) { get; } | Ruft eine übergeordnete Form für ab`TextBox` . |
| [Previous](../../aspose.words.drawing/textbox/previous/) { get; } | Gibt a zurück`TextBox` das repräsentiert das Vorherige`TextBox` in einer Folge von Formen. |
| [TextBoxWrapMode](../../aspose.words.drawing/textbox/textboxwrapmode/) { get; set; } | Bestimmt, wie Text innerhalb einer Form umbrochen wird. |
| [VerticalAnchor](../../aspose.words.drawing/textbox/verticalanchor/) { get; set; } | Gibt die vertikale Ausrichtung des Textes innerhalb einer Form an. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [BreakForwardLink](../../aspose.words.drawing/textbox/breakforwardlink/)() | Unterbricht die Verbindung zum nächsten`TextBox` . |
| [IsValidLinkTarget](../../aspose.words.drawing/textbox/isvalidlinktarget/)(TextBox) | Legt fest, ob dies der Fall ist`TextBox` kann mit dem Ziel verknüpft werden`TextBox` . |

### Bemerkungen

Benutzen Sie die[`TextBox`](../shape/textbox/) Eigenschaft, um auf Texteigenschaften einer Form zuzugreifen. Sie erstellen keine Instanzen davon`TextBox` Klasse direkt.

### Beispiele

Zeigt, wie interne Ränder für ein Textfeld festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein weiteres Textfeld mit bestimmten Rändern einfügen.
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

// Verschieben Sie den Dokument-Builder in die TextBox und fügen Sie Text hinzu.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Legen Sie die Eigenschaft „LayoutFlow“ fest, um eine Ausrichtung für den Textinhalt dieses Textfelds festzulegen.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

Zeigt, wie man die Größe eines Textfelds so anpasst, dass es genau in den Inhalt passt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Diese Werte auf diese beiden Elemente anwenden, damit die übergeordnete Form passt
// eng um den Textinhalt legen und dabei die von uns festgelegten Abmessungen ignorieren.
textBox.FitShapeToText = true;
textBox.TextBoxWrapMode = TextBoxWrapMode.None;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text fit tightly inside textbox.");

doc.Save(ArtifactsDir + "Shape.TextBoxFitShapeToText.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)


