---
title: Run.Run
second_title: Referencia de API de Aspose.Words para .NET
description: Run constructor. Inicializa una nueva instancia delRun clase.
type: docs
weight: 10
url: /es/net/aspose.words/run/run/
---
## Run(DocumentBase) {#constructor}

Inicializa una nueva instancia del[`Run`](../) clase.

```csharp
public Run(DocumentBase doc)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| doc | DocumentBase | El documento del propietario. |

### Observaciones

Cuando[`Run`](../) se crea, pertenece al documento especificado, pero aún no es parte del documento y[`ParentNode`](../../node/parentnode/) es`nulo`.

Para anexar[`Run`](../) al uso del documentoNode) oNode) en el párrafo donde desea insertar la ejecución.

### Ejemplos

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

* class [DocumentBase](../../documentbase/)
* class [Run](../)
* espacio de nombres [Aspose.Words](../../run/)
* asamblea [Aspose.Words](../../../)

---

## Run(DocumentBase, string) {#constructor_1}

Inicializa una nueva instancia del **Correr** clase.

```csharp
public Run(DocumentBase doc, string text)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| doc | DocumentBase | El documento del propietario. |
| text | String | El texto de la carrera. |

### Observaciones

Cuando[`Run`](../) se crea, pertenece al documento especificado, pero aún no es parte del documento y[`ParentNode`](../../node/parentnode/) es`nulo`.

Para anexar[`Run`](../) al uso del documentoNode) oNode) en el párrafo donde desea insertar la ejecución.

### Ejemplos

Muestra cómo dar formato a una serie de texto usando su propiedad de fuente.

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

### Ver también

* class [DocumentBase](../../documentbase/)
* class [Run](../)
* espacio de nombres [Aspose.Words](../../run/)
* asamblea [Aspose.Words](../../../)


