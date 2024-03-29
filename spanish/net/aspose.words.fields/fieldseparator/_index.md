---
title: FieldSeparator Class
linktitle: FieldSeparator
articleTitle: FieldSeparator
second_title: Aspose.Words para .NET
description: Aspose.Words.Fields.FieldSeparator clase. Representa un separador de campos de Word que separa el código de campo del resultado del campo en C#.
type: docs
weight: 2380
url: /es/net/aspose.words.fields/fieldseparator/
---
## FieldSeparator class

Representa un separador de campos de Word que separa el código de campo del resultado del campo.

Para obtener más información, visite el[Trabajar con campos](https://docs.aspose.com/words/net/working-with-fields/) artículo de documentación.

```csharp
public class FieldSeparator : FieldChar
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica el identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype/) { get; } | Devuelve el tipo de campo. |
| [Font](../../aspose.words/inline/font/) { get; } | Proporciona acceso al formato de fuente de este objeto. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Devoluciones`verdadero` si este nodo puede contener otros nodos. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Devuelve verdadero si este objeto se eliminó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Devuelve verdadero si se cambió el formato del objeto en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Devuelve verdadero si este objeto se insertó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked/) { get; set; } | Obtiene o establece si el campo principal está bloqueado (no debe volver a calcular su resultado). |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Devoluciones`verdadero` si este objeto se movió (eliminó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Devoluciones`verdadero` si este objeto se movió (insertó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words.fields/fieldseparator/nodetype/) { get; } | DevolucionesFieldSeparator . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Recupera el padre[`Paragraph`](../../aspose.words/paragraph/) de este nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un[`Range`](../../aspose.words/range/) objeto que representa la parte de un documento contenido en este nodo. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words.fields/fieldseparator/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Acepta un visitante. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicado del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Obtiene el primer ancestro del especificado[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtiene el primer antepasado del tipo de objeto especificado. |
| [GetField](../../aspose.words.fields/fieldchar/getfield/)() | Devuelve un campo para el campo char. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Obtiene el carácter especial que representa este nodo. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Obtiene el siguiente nodo según el algoritmo transversal del árbol de pedidos anticipados. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Obtiene el nodo anterior según el algoritmo transversal del árbol de pedidos anticipados. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina del padre. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |

## Observaciones

`FieldSeparator` es un nodo de nivel en línea y representado por el[`FieldSeparatorChar`](../../aspose.words/controlchar/fieldseparatorchar/) carácter de control en el documento.

`FieldSeparator` sólo puede ser hijo de[`Paragraph`](../../aspose.words/paragraph/).

Un campo completo en un documento de Microsoft Word es una estructura compleja que consta de un carácter de inicio de campo, un código de campo, un carácter separador de campo, un resultado de campo y un carácter de fin de campo. Algunos campos solo tienen inicio de campo, código de campo y final de campo.

Para insertar fácilmente un nuevo campo en un documento, utilice el[`InsertField`](../../aspose.words/documentbuilder/insertfield/) Método .

## Ejemplos

Muestra cómo trabajar con una colección de campos.

```csharp
public void FieldCollection()
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

    // Iterar sobre la colección de campos e imprimir contenidos y escribir
    // de cada campo utilizando una implementación de visitante personalizada.
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
}

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
    /// Obtiene el texto sin formato del documento acumulado por el visitante.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo FieldStart en el documento.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo FieldSeparator en el documento.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo FieldEnd en el documento.
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

* class [FieldChar](../fieldchar/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)
