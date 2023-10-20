---
title: ParagraphAlignment Enum
linktitle: ParagraphAlignment
articleTitle: ParagraphAlignment
second_title: Aspose.Words para .NET
description: Aspose.Words.ParagraphAlignment enumeración. Especifica la alineación del texto en un párrafo en C#.
type: docs
weight: 4400
url: /es/net/aspose.words/paragraphalignment/
---
## ParagraphAlignment enumeration

Especifica la alineación del texto en un párrafo.

```csharp
public enum ParagraphAlignment
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Left | `0` | El texto está alineado a la izquierda. |
| Center | `1` | El texto está centrado horizontalmente. |
| Right | `2` | El texto está alineado a la derecha. |
| Justify | `3` | El texto está alineado tanto a la izquierda como a la derecha. |
| Distributed | `4` | El texto está distribuido uniformemente. |
| ArabicMediumKashida | `5` | Solo árabe. La longitud de Kashida para el texto se extiende a una longitud media determinada por el consumidor. |
| ArabicHighKashida | `7` | Solo árabe. La longitud de Kashida para el texto se extiende a su longitud más amplia posible. |
| ArabicLowKashida | `8` | Solo árabe. La longitud de Kashida para el texto se amplía a una longitud ligeramente mayor. |
| ThaiDistributed | `9` | Solo tailandés. El texto está justificado con una optimización para tailandés. |
| MathElementCenterAsGroup | `10` | El único elemento matemático en una línea, alineado como 'Centrado como grupo'. |

## Ejemplos

Muestra cómo construir un documento Aspose.Words a mano.

```csharp
Document doc = new Document();

// Un documento en blanco contiene una sección, un cuerpo y un párrafo.
// Llama al método "RemoveAllChildren" para eliminar todos esos nodos,
// y terminar con un nodo de documento sin hijos.
doc.RemoveAllChildren();

// Este documento ahora no tiene nodos secundarios compuestos a los que podamos agregar contenido.
// Si deseamos editarlo, necesitaremos volver a llenar su colección de nodos.
// Primero, crea una nueva sección y luego agrégala como secundaria al nodo del documento raíz.
Section section = new Section(doc);
doc.AppendChild(section);

// Establece algunas propiedades de configuración de página para la sección.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Una sección necesita un cuerpo, que contendrá y mostrará todo su contenido
// en la página entre el encabezado y el pie de página de la sección.
Body body = new Body(doc);
section.AppendChild(body);

// Crea un párrafo, establece algunas propiedades de formato y luego añádelo como elemento secundario al cuerpo.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Finalmente, agrega algo de contenido para hacer el documento. Crea una carrera,
// establece su apariencia y contenido, y luego lo agrega como elemento secundario al párrafo.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
