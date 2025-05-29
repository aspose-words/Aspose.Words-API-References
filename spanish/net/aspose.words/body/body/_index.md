---
title: Body
linktitle: Body
articleTitle: Body
second_title: Aspose.Words para .NET
description: Crea y personaliza fácilmente una nueva instancia de Body con nuestro constructor intuitivo. ¡Experimenta hoy mismo una integración perfecta en tus proyectos!
type: docs
weight: 10
url: /es/net/aspose.words/body/body/
---
## Body constructor

Inicializa una nueva instancia del[`Body`](../) clase.

```csharp
public Body(DocumentBase doc)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| doc | DocumentBase | El documento del propietario. |

## Observaciones

Cuando[`Body`](../) se crea, pertenece al documento especificado, pero aún no es parte del documento y[`ParentNode`](../../node/parentnode/) es`nulo`.

Para anexar[`Body`](../) un[`Section`](../../section/) usar[`AnexarNiño`](../../compositenode/appendchild/)[`Insertar después`](../../compositenode/insertafter/) o[`Insertar antes`](../../compositenode/insertbefore/) métodos.

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
* class [Body](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
