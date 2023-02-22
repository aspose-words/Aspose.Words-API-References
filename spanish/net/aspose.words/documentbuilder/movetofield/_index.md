---
title: DocumentBuilder.MoveToField
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentBuilder método. Mueve el cursor a un campo del documento.
type: docs
weight: 510
url: /es/net/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder.MoveToField method

Mueve el cursor a un campo del documento.

```csharp
public void MoveToField(Field field, bool isAfter)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| field | Field | El campo al que mover el cursor. |
| isAfter | Boolean | Cuando es verdadero, mueve el cursor para que esté después del final del campo. Cuando es falso, mueve el cursor para que esté antes del inicio del campo. |

### Ejemplos

Muestra cómo mover el cursor del punto de inserción de un nodo del generador de documentos a un campo específico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte un campo usando DocumentBuilder y agregue una secuencia de texto después de él.
Field field = builder.InsertField(" AUTHOR \"John Doe\" ");

// El cursor del constructor está actualmente al final del documento.
Assert.Null(builder.CurrentNode);

// Mueva el cursor al campo mientras especifica si colocar ese cursor antes o después del campo.
builder.MoveToField(field, moveCursorToAfterTheField);

// Tenga en cuenta que el cursor está fuera del campo en ambos casos.
// Esto significa que no podemos editar el campo usando el constructor de esta manera.
// Para editar un campo, podemos usar el método MoveTo del constructor en el FieldStart de un campo
// o nodo FieldSeparator para colocar el cursor dentro.
if (moveCursorToAfterTheField)
{
    Assert.Null(builder.CurrentNode);
    builder.Write(" Text immediately after the field.");

    Assert.AreEqual("\u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015 Text immediately after the field.", 
        doc.GetText().Trim());
}
else
{
    Assert.AreEqual(field.Start, builder.CurrentNode);
    builder.Write("Text immediately before the field. ");

    Assert.AreEqual("Text immediately before the field. \u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015", 
        doc.GetText().Trim());
}
```

### Ver también

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)


