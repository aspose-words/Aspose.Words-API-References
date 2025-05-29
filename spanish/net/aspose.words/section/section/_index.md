---
title: Section
linktitle: Section
articleTitle: Section
second_title: Aspose.Words para .NET
description: Crea secciones web dinámicas fácilmente con nuestro Constructor de Secciones. Inicializa y personaliza fácilmente tu clase de Sección para optimizar el rendimiento de tu sitio web.
type: docs
weight: 10
url: /es/net/aspose.words/section/section/
---
## Section constructor

Inicializa una nueva instancia de la clase Section.

```csharp
public Section(DocumentBase doc)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| doc | DocumentBase | El documento del propietario. |

## Observaciones

Cuando se crea la sección, pertenece al documento especificado, pero aún no es parte del documento y[`ParentNode`](../../node/parentnode/) es`nulo`.

Para incluir[`Section`](../) en un documento de uso[`InsertAfter`](../../compositenode/insertafter/) y [`InsertBefore`](../../compositenode/insertbefore/) métodos de la[`Document`](../../document/) OR [`Add`](../../nodecollection/add/) y[`Insert`](../../nodecollection/insert/) métodos de la[`Sections`](../../document/sections/) propiedad.

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

### Ver también

* class [DocumentBase](../../documentbase/)
* class [Section](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
