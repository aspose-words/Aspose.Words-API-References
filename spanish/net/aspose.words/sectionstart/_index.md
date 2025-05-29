---
title: SectionStart Enum
linktitle: SectionStart
articleTitle: SectionStart
second_title: Aspose.Words para .NET
description: Explore la enumeración Aspose.Words.SectionStart para comprender los saltos de sección y mejorar el formato del documento para un mejor control y presentación.
type: docs
weight: 6590
url: /es/net/aspose.words/sectionstart/
---
## SectionStart enumeration

El tipo de salto al inicio de la sección.

```csharp
public enum SectionStart
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Continuous | `0` | La nueva sección comienza en la misma página que la sección anterior. |
| NewColumn | `1` | La sección comienza desde una nueva columna. |
| NewPage | `2` | La sección comienza desde una nueva página. |
| EvenPage | `3` | La sección comienza en una nueva página par. |
| OddPage | `4` | La sección comienza en una nueva página impar. |

## Ejemplos

Muestra cómo construir un documento Aspose.Words a mano.

```csharp
Document doc = new Document();

// Un documento en blanco contiene una sección, un cuerpo y un párrafo.
// Llama al método "RemoveAllChildren" para eliminar todos esos nodos,
// y terminar con un nodo de documento sin hijos.
doc.RemoveAllChildren();

//Este documento ahora no tiene nodos secundarios compuestos a los que podamos agregar contenido.
// Si deseamos editarlo, necesitaremos volver a llenar su colección de nodos.
// Primero, cree una nueva sección y luego añádala como un elemento secundario al nodo del documento raíz.
Section section = new Section(doc);
doc.AppendChild(section);

// Establezca algunas propiedades de configuración de página para la sección.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Una sección necesita un cuerpo, que contendrá y mostrará todo su contenido.
// en la página entre el encabezado y el pie de página de la sección.
Body body = new Body(doc);
section.AppendChild(body);

// Cree un párrafo, establezca algunas propiedades de formato y luego añádalo como elemento secundario al cuerpo.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Finalmente, agrega algo de contenido para completar el documento. Crea una ejecución.
// establece su apariencia y contenido, y luego lo agrega como un elemento secundario al párrafo.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

Muestra cómo especificar cómo una nueva sección se separa de la anterior.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("This text is in section 1.");

// Los tipos de salto de sección determinan cómo una nueva sección se separa de la sección anterior.
// A continuación se muestran cinco tipos de saltos de sección.
// 1 - Inicia la siguiente sección en una nueva página:
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("This text is in section 2.");

Assert.AreEqual(SectionStart.NewPage, doc.Sections[1].PageSetup.SectionStart);

// 2 - Inicia la siguiente sección en la página actual:
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("This text is in section 3.");

Assert.AreEqual(SectionStart.Continuous, doc.Sections[2].PageSetup.SectionStart);

// 3 - Inicia la siguiente sección en una nueva página par:
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Writeln("This text is in section 4.");

Assert.AreEqual(SectionStart.EvenPage, doc.Sections[3].PageSetup.SectionStart);

// 4 - Comienza la siguiente sección en una nueva página impar:
builder.InsertBreak(BreakType.SectionBreakOddPage);
builder.Writeln("This text is in section 5.");

Assert.AreEqual(SectionStart.OddPage, doc.Sections[4].PageSetup.SectionStart);

// 5 - Inicia la siguiente sección en una nueva columna:
TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.SetCount(2);

builder.InsertBreak(BreakType.SectionBreakNewColumn);
builder.Writeln("This text is in section 6.");

Assert.AreEqual(SectionStart.NewColumn, doc.Sections[5].PageSetup.SectionStart);

doc.Save(ArtifactsDir + "PageSetup.SetSectionStart.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
