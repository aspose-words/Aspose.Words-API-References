---
title: Document.UpdateWordCount
linktitle: UpdateWordCount
articleTitle: UpdateWordCount
second_title: Aspose.Words para .NET
description: Mejore la eficiencia de su documento con el método UpdateWordCount, garantizando propiedades de recuento de palabras precisas para una mejor edición y revisión.
type: docs
weight: 850
url: /es/net/aspose.words/document/updatewordcount/
---
## UpdateWordCount() {#updatewordcount}

Actualiza las propiedades de recuento de palabras del documento.

```csharp
public void UpdateWordCount()
```

## Observaciones

`UpdateWordCount` recalcula y actualiza las propiedades Caracteres, Palabras y Párrafos en el[`BuiltInDocumentProperties`](../builtindocumentproperties/) colección de la[`Document`](../).

Tenga en cuenta que`UpdateWordCount` no actualiza el número de líneas y propiedades de páginas. Utilice el`UpdateWordCount` sobrecarga y pase`verdadero` valor como parámetro para hacer eso.

Cuando utilice una versión de evaluación, la marca de agua de evaluación también se incluirá en el recuento de palabras.

## Ejemplos

Muestra cómo actualizar todas las etiquetas de lista en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words no realiza un seguimiento de métricas de documentos como estas en tiempo real.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// Para obtener valores precisos para tres de estas propiedades, necesitaremos actualizarlas manualmente.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// Para el conteo de líneas, necesitaremos llamar a una sobrecarga específica del método de actualización.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## UpdateWordCount(*bool*) {#updatewordcount_1}

Actualiza las propiedades de recuento de palabras del documento, actualiza opcionalmente[`Lines`](../../../aspose.words.properties/builtindocumentproperties/lines/) propiedad.

```csharp
public void UpdateWordCount(bool updateLinesCount)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| updateLinesCount | Boolean | `verdadero` Si se debe calcular el número de líneas del documento. |

## Observaciones

Este método reconstruirá el diseño de página del documento.

## Ejemplos

Muestra cómo actualizar todas las etiquetas de lista en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words no realiza un seguimiento de métricas de documentos como estas en tiempo real.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// Para obtener valores precisos para tres de estas propiedades, necesitaremos actualizarlas manualmente.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// Para el conteo de líneas, necesitaremos llamar a una sobrecarga específica del método de actualización.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
