---
title: EditableRange.EditableRangeEnd
linktitle: EditableRangeEnd
articleTitle: EditableRangeEnd
second_title: Aspose.Words para .NET
description: Descubra la propiedad EditableRangeEnd, acceda fácilmente al nodo que marca el final de su rango editable para una gestión de contenido perfecta.
type: docs
weight: 10
url: /es/net/aspose.words/editablerange/editablerangeend/
---
## EditableRange.EditableRangeEnd property

Obtiene el nodo que representa el final del rango editable.

```csharp
public EditableRangeEnd EditableRangeEnd { get; }
```

## Ejemplos

Muestra cómo trabajar con un rango editable.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// Los rangos editables nos permiten dejar partes de documentos protegidos abiertas para su edición.
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

// Un rango editable bien formado tiene un nodo inicial y un nodo final.
// Estos nodos tienen identificaciones coincidentes y abarcan nodos editables.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// Las diferentes partes del rango editable se vinculan entre sí.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

Podemos acceder a los tipos de nodo de cada parte de esta manera. El rango editable en sí no es un nodo.
// sino una entidad que consta de un inicio, un final y sus contenidos incluidos.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// Eliminar un rango editable. Todos los nodos dentro del rango permanecerán intactos.
editableRange.Remove();
```

### Ver también

* class [EditableRangeEnd](../../editablerangeend/)
* class [EditableRange](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
