---
title: ControlChar.NonBreakingSpaceChar
linktitle: NonBreakingSpaceChar
articleTitle: NonBreakingSpaceChar
second_title: Aspose.Words para .NET
description: ControlChar NonBreakingSpaceChar campo. Carácter de espacio de no separación char160 en C#.
type: docs
weight: 180
url: /es/net/aspose.words/controlchar/nonbreakingspacechar/
---
## ControlChar.NonBreakingSpaceChar field

Carácter de espacio de no separación: (char)160.

```csharp
public const char NonBreakingSpaceChar;
```

## Ejemplos

Muestra cómo agregar varios caracteres de control a un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Agrega un espacio normal.
builder.Write("Before space." + ControlChar.SpaceChar + "After space.");

// Agrega un NBSP, que es un espacio sin separación.
// A diferencia del espacio normal, este espacio no puede tener un salto de línea automático en su posición.
builder.Write("Before space." + ControlChar.NonBreakingSpace + "After space.");

// Agrega un carácter de tabulación.
builder.Write("Before tab." + ControlChar.Tab + "After tab.");

// Agrega un salto de línea.
builder.Write("Before line break." + ControlChar.LineBreak + "After line break.");

// Agrega una nueva línea y comienza un nuevo párrafo.
Assert.AreEqual(1, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);
builder.Write("Before line feed." + ControlChar.LineFeed + "After line feed.");
Assert.AreEqual(2, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// El carácter de avance de línea tiene dos versiones.
Assert.AreEqual(ControlChar.LineFeed, ControlChar.Lf);

// Los retornos de carro y los avances de línea se pueden representar juntos mediante un carácter.
Assert.AreEqual(ControlChar.CrLf, ControlChar.Cr + ControlChar.Lf);

// Agrega un salto de párrafo, que iniciará un nuevo párrafo.
builder.Write("Before paragraph break." + ControlChar.ParagraphBreak + "After paragraph break.");
Assert.AreEqual(3, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// Agrega un salto de sección. Esto no crea una nueva sección o párrafo.
Assert.AreEqual(1, doc.Sections.Count);
builder.Write("Before section break." + ControlChar.SectionBreak + "After section break.");
Assert.AreEqual(1, doc.Sections.Count);

// Agrega un salto de página.
builder.Write("Before page break." + ControlChar.PageBreak + "After page break.");

// Un salto de página tiene el mismo valor que un salto de sección.
Assert.AreEqual(ControlChar.PageBreak, ControlChar.SectionBreak);

// Inserta una nueva sección y luego establece el número de columnas en dos.
doc.AppendChild(new Section(doc));
builder.MoveToSection(1);
builder.CurrentSection.PageSetup.TextColumns.SetCount(2);

// Podemos usar un carácter de control para marcar el punto donde el texto pasa a la siguiente columna.
builder.Write("Text at end of column 1." + ControlChar.ColumnBreak + "Text at beginning of column 2.");

doc.Save(ArtifactsDir + "ControlChar.InsertControlChars.docx");

// Hay contrapartes de caracteres y cadenas para la mayoría de los caracteres.
Assert.AreEqual(Convert.ToChar(ControlChar.Cell), ControlChar.CellChar);
Assert.AreEqual(Convert.ToChar(ControlChar.NonBreakingSpace), ControlChar.NonBreakingSpaceChar);
Assert.AreEqual(Convert.ToChar(ControlChar.Tab), ControlChar.TabChar);
Assert.AreEqual(Convert.ToChar(ControlChar.LineBreak), ControlChar.LineBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.LineFeed), ControlChar.LineFeedChar);
Assert.AreEqual(Convert.ToChar(ControlChar.ParagraphBreak), ControlChar.ParagraphBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.SectionBreak), ControlChar.SectionBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.PageBreak), ControlChar.SectionBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.ColumnBreak), ControlChar.ColumnBreakChar);
```

### Ver también

* class [ControlChar](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
