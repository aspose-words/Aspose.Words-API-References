---
title: CompositeNode.AppendChild
linktitle: AppendChild
articleTitle: AppendChild
second_title: Aspose.Words para .NET
description: CompositeNode AppendChild método. Agrega el nodo especificado al final de la lista de nodos secundarios para este nodo en C#.
type: docs
weight: 60
url: /es/net/aspose.words/compositenode/appendchild/
---
## CompositeNode.AppendChild method

Agrega el nodo especificado al final de la lista de nodos secundarios para este nodo.

```csharp
public Node AppendChild(Node newChild)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| newChild | Node | El nodo a agregar. |

### Valor_devuelto

Agregó el nodo.

## Observaciones

Si el*newChild* ya está en el árbol, primero se elimina.

Si el nodo que se está insertando se creó a partir de otro documento, debe usar [`ImportNode`](../../documentbase/importnode/) para importar el nodo al documento actual. El nodo importado luego se puede insertar en el documento actual.

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

* class [Node](../../node/)
* class [CompositeNode](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
