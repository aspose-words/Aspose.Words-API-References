---
title: ShapeBase.WrapType
linktitle: WrapType
articleTitle: WrapType
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShapeBase WrapType, controlla le forme in linea o mobili e personalizza l'avvolgimento del testo per una maggiore flessibilità di layout.
type: docs
weight: 640
url: /it/net/aspose.words.drawing/shapebase/wraptype/
---
## ShapeBase.WrapType property

Definisce se la forma è in linea o mobile. Per le forme mobili, definisce la modalità di avvolgimento del testo attorno alla forma.

```csharp
public WrapType WrapType { get; set; }
```

## Osservazioni

Il valore predefinito èNone.

Ha effetto solo sulle forme di livello superiore.

## Esempi

Mostra come inserire un'immagine mobile al centro di una pagina.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un'immagine mobile che apparirà dietro il testo sovrapposto e allineala al centro della pagina.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Mostra come creare e formattare una casella di testo.

```csharp
Document doc = new Document();

// Crea una casella di testo mobile.
Shape textBox = new Shape(doc, ShapeType.TextBox);
textBox.WrapType = WrapType.None;
textBox.Height = 50;
textBox.Width = 200;

// Imposta l'allineamento orizzontale e verticale del testo all'interno della forma.
textBox.HorizontalAlignment = HorizontalAlignment.Center;
textBox.VerticalAlignment = VerticalAlignment.Top;

// Aggiungere un paragrafo alla casella di testo e aggiungere una sequenza di testo che verrà visualizzata nella casella di testo.
textBox.AppendChild(new Paragraph(doc));
Paragraph para = textBox.FirstParagraph;
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;
Run run = new Run(doc);
run.Text = "Hello world!";
para.AppendChild(run);

doc.FirstSection.Body.FirstParagraph.AppendChild(textBox);

doc.Save(ArtifactsDir + "Shape.CreateTextBox.docx");
```

### Guarda anche

* enum [WrapType](../../wraptype/)
* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
