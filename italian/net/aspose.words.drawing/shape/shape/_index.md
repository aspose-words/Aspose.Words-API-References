---
title: Shape
linktitle: Shape
articleTitle: Shape
second_title: Aspose.Words per .NET
description: Crea oggetti di forma unici senza sforzo con il nostro Shape Constructor. Progetta forme personalizzate e migliora i tuoi progetti con facilità e precisione!
type: docs
weight: 10
url: /it/net/aspose.words.drawing/shape/shape/
---
## Shape constructor

Crea un nuovo oggetto forma.

```csharp
public Shape(DocumentBase doc, ShapeType shapeType)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | DocumentBase | Il documento del proprietario. |
| shapeType | ShapeType | Il tipo di forma da creare. |

## Osservazioni

Dopo aver creato una forma, è necessario specificare le proprietà desiderate.

## Esempi

Mostra come inserire una forma con un'immagine dal file system locale in un documento.

```csharp
Document doc = new Document();

// Il costruttore pubblico della classe "Shape" creerà una forma con tipo di markup "ShapeMarkupLanguage.Vml".
// Se è necessario creare una forma di tipo non primitivo, come SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// AngoliTopUnoArrotondatoUnoTagliato, AngoloSingoloArrotondato, AngoliTopArrotondati o AngoliDiagonaliArrotondati,
// si prega di utilizzare DocumentBuilder.InsertShape.
Shape shape = new Shape(doc, ShapeType.Image);
shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
shape.Width = 100;
shape.Height = 100;

doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

doc.Save(ArtifactsDir + "Image.FromFile.docx");
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

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [ShapeType](../../shapetype/)
* class [Shape](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
