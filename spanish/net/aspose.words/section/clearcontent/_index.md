---
title: Section.ClearContent
second_title: Referencia de API de Aspose.Words para .NET
description: Section método. Borra la sección.
type: docs
weight: 110
url: /es/net/aspose.words/section/clearcontent/
---
## Section.ClearContent method

Borra la sección.

```csharp
public void ClearContent()
```

### Observaciones

el texto de[`Body`](../body/) se borra, solo queda un párrafo vacío que representa el salto de sección.

Se borra el texto de todos los encabezados y pies de página, pero[`HeaderFooter`](../../headerfooter/) Los objetos en sí no se eliminan.

### Ejemplos

Muestra cómo borrar el contenido de una sección.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Al ejecutar el método "ClearContent" se eliminarán todos los contenidos de la sección
// pero deja un párrafo en blanco para agregar contenido nuevamente.
doc.FirstSection.ClearContent();

Assert.AreEqual(string.Empty, doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);
```

### Ver también

* class [Section](../)
* espacio de nombres [Aspose.Words](../../section/)
* asamblea [Aspose.Words](../../../)


