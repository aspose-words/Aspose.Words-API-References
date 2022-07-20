---
title: Item
second_title: Referencia de API de Aspose.Words para .NET
description: Recupera una sección en el índice dado.
type: docs
weight: 10
url: /es/net/aspose.words/sectioncollection/item/
---
## SectionCollection indexer

Recupera una sección en el índice dado.

```csharp
public Section this[int index] { get; }
```

| Parámetro | Descripción |
| --- | --- |
| index | Un índice en la lista de secciones. |

### Observaciones

El índice está basado en cero.

Los índices negativos están permitidos e indican el acceso desde la parte posterior de la colección. Por ejemplo, -1 significa el último elemento, -2 significa el penúltimo y así sucesivamente.

Si el índice es mayor o igual que el número de elementos en la lista, esto devuelve una referencia nula.

Si el índice es negativo y su valor absoluto es mayor que el número de elementos de la lista, esto devuelve una referencia nula.

### Ejemplos

Muestra cuándo recalcular el diseño de página del documento.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Guardar un documento en PDF, en una imagen o imprimirlo por primera vez automáticamente
// almacena en caché el diseño del documento dentro de sus páginas.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Modificar el documento de alguna manera.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;

  // En la versión actual de Aspose.Words, la modificación del documento no se reconstruye automáticamente
// el diseño de la página en caché. Si deseamos el diseño en caché
// para estar actualizado, necesitaremos actualizarlo manualmente.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

Muestra cómo preparar un nuevo nodo de sección para su edición.

```csharp
Document doc = new Document();

// Un documento en blanco viene con una sección, que tiene un cuerpo, que a su vez tiene un párrafo.
// Podemos agregar contenido a este documento agregando elementos como líneas de texto, formas o tablas a ese párrafo.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Si agregamos una nueva sección como esta, no tendrá un cuerpo ni ningún otro nodo secundario.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Ejecute el método "EnsureMinimum" para agregar un cuerpo y un párrafo a esta sección para comenzar a editarla.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ver también

* class [Section](../../section)
* class [SectionCollection](../../sectioncollection)
* espacio de nombres [Aspose.Words](../../sectioncollection)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->