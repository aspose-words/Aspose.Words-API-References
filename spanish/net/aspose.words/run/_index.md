---
title: Run
second_title: Referencia de API de Aspose.Words para .NET
description: Representa una serie de caracteres con el mismo formato de fuente.
type: docs
weight: 4560
url: /es/net/aspose.words/run/
---
## Run class

Representa una serie de caracteres con el mismo formato de fuente.

```csharp
public class Run : Inline
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [Run](run#constructor)(DocumentBase) | Inicializa una nueva instancia del **Correr** clase. |
| [Run](run#constructor_1)(DocumentBase, string) | Inicializa una nueva instancia del **Correr** clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Especifica el identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document) { get; } | Obtiene el documento al que pertenece este nodo. |
| [Font](../../aspose.words/inline/font) { get; } | Proporciona acceso al formato de fuente de este objeto. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Devuelve verdadero si este nodo puede contener otros nodos. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision) { get; } | Devuelve verdadero si este objeto se eliminó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision) { get; } | Devuelve verdadero si se cambió el formato del objeto en Microsoft Word mientras estaba habilitado el seguimiento de cambios. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision) { get; } | Devuelve verdadero si este objeto se insertó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision) { get; } | Devoluciones **verdadero** si este objeto se movió (eliminó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision) { get; } | Devoluciones **verdadero** si este objeto se movió (insertó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words/run/nodetype) { get; } | Devoluciones **NodeType.Ejecutar** . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Obtiene el padre inmediato de este nodo. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph) { get; } | Recupera el padre[`Paragraph`](../paragraph) de este nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range) { get; } | Devuelve un **Rango** objeto que representa la parte de un documento que está contenido en este nodo. |
| [Text](../../aspose.words/run/text) { get; set; } | Obtiene o establece el texto de la ejecución. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words/run/accept)(DocumentVisitor) | Acepta un visitante. |
| [Clone](../../aspose.words/node/clone)(bool) | Crea un duplicado del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Obtiene el primer ancestro del especificado[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Obtiene el primer ancestro del tipo de objeto especificado. |
| override [GetText](../../aspose.words/run/gettext)() | Obtiene el texto de la ejecución. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Obtiene el siguiente nodo de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Obtiene el nodo anterior de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [Remove](../../aspose.words/node/remove)() | Se elimina a sí mismo del padre. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exporta el contenido del nodo a una cadena utilizando las opciones de guardado especificadas. |

### Observaciones

Todo el texto del documento se almacena en tiradas de texto.

**Correr** solo puede ser hijo de **Párrafo** o en línea **Etiqueta de documento estructurado**.

### Ejemplos

Muestra cómo dar formato a una tirada de texto utilizando su propiedad de fuente.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

Muestra cómo construir un documento de Aspose.Words a mano.

```csharp
Document doc = new Document();

// Un documento en blanco contiene una sección, un cuerpo y un párrafo.
// Llame al método "RemoveAllChildren" para eliminar todos esos nodos,
// y terminar con un nodo de documento sin hijos.
doc.RemoveAllChildren();

// Este documento ahora no tiene nodos secundarios compuestos a los que podamos agregar contenido.
// Si deseamos editarlo, necesitaremos volver a llenar su colección de nodos.
// Primero, cree una nueva sección y luego agréguela como elemento secundario al nodo del documento raíz.
Section section = new Section(doc);
doc.AppendChild(section);

// Establecer algunas propiedades de configuración de página para la sección.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Una sección necesita un cuerpo, que contendrá y mostrará todo su contenido
// en la página entre el encabezado y el pie de página de la sección.
Body body = new Body(doc);
section.AppendChild(body);

// Cree un párrafo, establezca algunas propiedades de formato y luego agréguelo como elemento secundario al cuerpo.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Finalmente, agregue algo de contenido para hacer el documento. Crear una carrera,
// establece su apariencia y contenido, y luego lo agrega como elemento secundario al párrafo.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

Muestra cómo agregar, actualizar y eliminar nodos secundarios en la colección de elementos secundarios de CompositeNode.

```csharp
Document doc = new Document();

// Un documento vacío, por defecto, tiene un párrafo.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Los nodos compuestos como nuestro párrafo pueden contener otros nodos compuestos y en línea como elementos secundarios.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Crea tres nodos de ejecución más.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// El cuerpo del documento no mostrará estas ejecuciones hasta que las insertemos en un nodo compuesto
// eso en sí mismo es parte del árbol de nodos del documento, como hicimos con la primera ejecución.
// Podemos determinar donde esta el contenido de texto de los nodos que insertamos
// aparece en el documento especificando una ubicación de inserción relativa a otro nodo en el párrafo.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Inserta la segunda ejecución en el párrafo delante de la ejecución inicial.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Inserta la tercera ejecución después de la ejecución inicial.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Inserta la primera ejecución al comienzo de la colección de nodos secundarios del párrafo.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Podemos modificar el contenido de la ejecución editando y eliminando los nodos secundarios existentes.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Ver también

* class [Inline](../inline)
* espacio de nombres [Aspose.Words](../../aspose.words)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
