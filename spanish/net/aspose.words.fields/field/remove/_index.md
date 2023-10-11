---
title: Field.Remove
second_title: Referencia de API de Aspose.Words para .NET
description: Field método. Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo principal devuelve su párrafo principal. Si el campo ya está eliminado devuelvenulo .
type: docs
weight: 120
url: /es/net/aspose.words.fields/field/remove/
---
## Field.Remove method

Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo principal, devuelve su párrafo principal. Si el campo ya está eliminado, devuelve`nulo` .

```csharp
public Node Remove()
```

### Ejemplos

Muestra cómo eliminar campos de una colección de campos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder.InsertField(" TIME ");
builder.InsertField(" REVNUM ");
builder.InsertField(" AUTHOR  \"John Doe\" ");
builder.InsertField(" SUBJECT \"My Subject\" ");
builder.InsertField(" QUOTE \"Hello world!\" ");
doc.UpdateFields();

FieldCollection fields = doc.Range.Fields;

Assert.AreEqual(6, fields.Count);

// A continuación se muestran cuatro formas de eliminar campos de una colección de campos.
// 1 - Obtener un campo para eliminarse a sí mismo:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Obtener la colección para eliminar un campo que pasamos a su método de eliminación:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - Eliminar un campo de una colección en un índice:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - Elimina todos los campos de la colección a la vez:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

Muestra cómo procesar campos PRIVADOS.

```csharp
public void FieldPrivate()
{
    // Abre un documento de Corel WordPerfect que hemos convertido al formato .docx.
    Document doc = new Document(MyDir + "Field sample - PRIVATE.docx");

    // Los documentos WordPerfect 5.x/6.x como el que hemos cargado pueden contener campos PRIVADOS.
    // Microsoft Word conserva los campos PRIVADOS durante las operaciones de carga/guardado,
    // pero no les proporciona ninguna funcionalidad.
    FieldPrivate field = (FieldPrivate)doc.Range.Fields[0];

    Assert.AreEqual(" PRIVATE \"My value\" ", field.GetFieldCode());
    Assert.AreEqual(FieldType.FieldPrivate, field.Type);

    // También podemos insertar campos PRIVADOS usando un generador de documentos.
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(FieldType.FieldPrivate, true);

    // Estos campos no son una forma viable de proteger información confidencial.
    // A menos que sea esencial la compatibilidad con versiones anteriores de WordPerfect,
    // podemos eliminar estos campos de forma segura. Podemos hacer esto usando una implementación de DocumentVisiitor.
    Assert.AreEqual(2, doc.Range.Fields.Count);

    FieldPrivateRemover remover = new FieldPrivateRemover();
    doc.Accept(remover);

    Assert.AreEqual(2, remover.GetFieldsRemovedCount());
    Assert.AreEqual(0, doc.Range.Fields.Count);
}

/// <summary>
/// Elimina todos los campos PRIVADOS encontrados.
/// </summary>
public class FieldPrivateRemover : DocumentVisitor
{
    public FieldPrivateRemover()
    {
        mFieldsRemovedCount = 0;
    }

    public int GetFieldsRemovedCount()
    {
        return mFieldsRemovedCount;
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo FieldEnd en el documento.
    /// Si el nodo pertenece a un campo PRIVADO, se elimina todo el campo.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.FieldType == FieldType.FieldPrivate)
        {
            fieldEnd.GetField().Remove();
            mFieldsRemovedCount++;
        }

        return VisitorAction.Continue;
    }

    private int mFieldsRemovedCount;
}
```

### Ver también

* class [Node](../../../aspose.words/node/)
* class [Field](../)
* espacio de nombres [Aspose.Words.Fields](../../field/)
* asamblea [Aspose.Words](../../../)


