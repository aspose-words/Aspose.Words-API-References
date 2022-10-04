---
title: FieldCollection
second_title: Referencia de API de Aspose.Words para .NET
description: Una colección deField./field/ objetos que representa los campos en el rango especificado.
type: docs
weight: 1540
url: /es/net/aspose.words.fields/fieldcollection/
---
## FieldCollection class

Una colección de[`Field`](../field/) objetos que representa los campos en el rango especificado.

```csharp
public class FieldCollection : IEnumerable<Field>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.fields/fieldcollection/count/) { get; } | Devuelve el número de campos de la colección. |
| [Item](../../aspose.words.fields/fieldcollection/item/) { get; } | Devuelve un campo en el índice especificado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Clear](../../aspose.words.fields/fieldcollection/clear/)() | Elimina todos los campos de esta colección del documento y de esta colección en sí. |
| [GetEnumerator](../../aspose.words.fields/fieldcollection/getenumerator/)() | Devuelve un objeto enumerador. |
| [Remove](../../aspose.words.fields/fieldcollection/remove/)(Field) | Elimina el campo especificado de esta colección y del documento. |
| [RemoveAt](../../aspose.words.fields/fieldcollection/removeat/)(int) | Elimina un campo en el índice especificado de esta colección y del documento. |

### Observaciones

Una instancia de esta colección itera los campos que comienzan dentro del rango especificado.

los[`FieldCollection`](./fieldcollection/) La colección no es propietaria de los campos que contiene, sino que es solo una selección de campos.

los[`FieldCollection`](./fieldcollection/) la colección está "viva", es decir, los cambios en los elementos secundarios del nodo object a partir del cual se creó se reflejan inmediatamente en los campos devueltos por el[`FieldCollection`](./fieldcollection/) propiedades y métodos.

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
// 1 - Obtener un campo para eliminarlo:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Obtener la colección para eliminar un campo que le pasamos a su método de eliminación:
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

Muestra cómo trabajar con una colección de campos.

```csharp
{
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

    // Iterar sobre la colección de campos e imprimir contenido y escribir
    // de cada campo usando una implementación de visitante personalizada.
    FieldVisitor fieldVisitor = new FieldVisitor();

    using (IEnumerator<Field> fieldEnumerator = fields.GetEnumerator())
    {
        while (fieldEnumerator.MoveNext())
        {
            if (fieldEnumerator.Current != null)
            {
                fieldEnumerator.Current.Start.Accept(fieldVisitor);
                fieldEnumerator.Current.Separator?.Accept(fieldVisitor);
                fieldEnumerator.Current.End.Accept(fieldVisitor);
            }
            else
            {
                Console.WriteLine("There are no fields in the document.");
            }
        }
    }

    Console.WriteLine(fieldVisitor.GetText());

/// <summary>
/// Implementación del visitante del documento que imprime la información del campo.
/// </summary>
public class FieldVisitor : DocumentVisitor
{
    public FieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Obtiene el texto sin formato del documento que fue acumulado por el visitante.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo FieldStart en el documento.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo FieldSeparator en el documento.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo FieldEnd en el documento.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mBuilder.AppendLine("End of field: " + fieldEnd.FieldType);

        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

### Ver también

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
