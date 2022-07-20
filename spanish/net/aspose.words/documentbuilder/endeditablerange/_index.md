---
title: EndEditableRange
second_title: Referencia de API de Aspose.Words para .NET
description: Marca la posición actual en el documento como un final de rango editable.
type: docs
weight: 210
url: /es/net/aspose.words/documentbuilder/endeditablerange/
---
## EndEditableRange() {#endeditablerange}

Marca la posición actual en el documento como un final de rango editable.

```csharp
public EditableRangeEnd EndEditableRange()
```

### Valor_devuelto

El nodo final del rango editable que se acaba de crear.

### Observaciones

El rango editable en un documento puede superponerse y abarcar cualquier rango. Para crear un rango editable válido, debe llamar a ambos[`StartEditableRange`](../starteditablerange) y`EndEditableRange` o[`EndEditableRange`](../endeditablerange)métodos.

El rango editable mal formado se ignorará cuando se guarde el documento.

### Ejemplos

Muestra cómo trabajar con un rango editable.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// Los rangos editables nos permiten dejar partes de documentos protegidos abiertos para su edición.
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

// Un rango editable bien formado tiene un nodo inicial y un nodo final.
// Estos nodos tienen ID coincidentes y abarcan nodos editables.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// Diferentes partes del rango editable se vinculan entre sí.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// Podemos acceder a los tipos de nodos de cada parte así. El rango editable en sí no es un nodo,
// sino una entidad que consta de un comienzo, un final y sus contenidos adjuntos.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// Eliminar un rango editable. Todos los nodos que estaban dentro del rango permanecerán intactos.
editableRange.Remove();
```

### Ver también

* class [EditableRangeEnd](../../editablerangeend)
* class [DocumentBuilder](../../documentbuilder)
* espacio de nombres [Aspose.Words](../../documentbuilder)
* asamblea [Aspose.Words](../../../)

---

## EndEditableRange(EditableRangeStart) {#endeditablerange_1}

Marca la posición actual en el documento como un final de rango editable.

```csharp
public EditableRangeEnd EndEditableRange(EditableRangeStart start)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| start | EditableRangeStart | Este rango editable comienza. |

### Valor_devuelto

El nodo final del rango editable que se acaba de crear.

### Observaciones

Utilice esta sobrecarga durante la creación de rangos editables anidados.

El rango editable en un documento puede superponerse y abarcar cualquier rango. Para crear un rango editable válido, debe llamar a ambos[`StartEditableRange`](../starteditablerange) y[`EndEditableRange`](../endeditablerange) o`EndEditableRange`métodos.

El rango editable mal formado se ignorará cuando se guarde el documento.

### Ejemplos

Muestra cómo crear rangos editables anidados.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only, " +
                "we cannot edit this paragraph without the password.");

// Crea dos rangos editables anidados.
EditableRangeStart outerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside the outer editable range and can be edited.");

EditableRangeStart innerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

// Actualmente, el cursor de inserción del nodo del generador de documentos está en más de un rango editable en curso.
// Cuando queremos terminar un rango editable en esta situación,
// necesitamos especificar cuál de los rangos deseamos terminar pasando su nodo EditableRangeStart.
builder.EndEditableRange(innerEditableRangeStart);

builder.Writeln("This paragraph inside the outer editable range and can be edited.");

builder.EndEditableRange(outerEditableRangeStart);

builder.Writeln("This paragraph is outside any editable ranges, and cannot be edited.");

// Si una región de texto tiene dos rangos editables superpuestos con grupos específicos,
// el grupo combinado de usuarios excluidos por ambos grupos no puede editarlo.
outerEditableRangeStart.EditableRange.EditorGroup = EditorType.Everyone;
innerEditableRangeStart.EditableRange.EditorGroup = EditorType.Contributors;

doc.Save(ArtifactsDir + "EditableRange.Nested.docx");
```

### Ver también

* class [EditableRangeEnd](../../editablerangeend)
* class [EditableRangeStart](../../editablerangestart)
* class [DocumentBuilder](../../documentbuilder)
* espacio de nombres [Aspose.Words](../../documentbuilder)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->