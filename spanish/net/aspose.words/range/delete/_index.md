---
title: Range.Delete
linktitle: Delete
articleTitle: Delete
second_title: Aspose.Words para .NET
description: Elimina eficazmente todos los caracteres dentro de un rango específico con el método de eliminación de rango. ¡Simplifica tus tareas de edición de texto sin esfuerzo!
type: docs
weight: 70
url: /es/net/aspose.words/range/delete/
---
## Range.Delete method

Elimina todos los caracteres del rango.

```csharp
public void Delete()
```

## Ejemplos

Muestra cómo eliminar todos los nodos de un rango.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Agregue texto a la primera sección del documento y luego agregue otra sección.
builder.Write("Section 1. ");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Write("Section 2.");

Assert.AreEqual("Section 1. \fSection 2.", doc.GetText().Trim());

//Elimine la primera sección por completo eliminando todos los nodos
// dentro de su rango, incluida la sección misma.
doc.Sections[0].Range.Delete();

Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual("Section 2.", doc.GetText().Trim());
```

### Ver también

* class [Range](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
