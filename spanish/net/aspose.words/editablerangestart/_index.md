---
title: EditableRangeStart
second_title: Referencia de API de Aspose.Words para .NET
description: Representa el comienzo de un rango editable en un documento de Word.
type: docs
weight: 1290
url: /es/net/aspose.words/editablerangestart/
---
## EditableRangeStart class

Representa el comienzo de un rango editable en un documento de Word.

```csharp
public sealed class EditableRangeStart : Node
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica el identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [EditableRange](../../aspose.words/editablerangestart/editablerange/) { get; } | Obtiene el objeto de fachada que encapsula este inicio y fin de rango editable. |
| [Id](../../aspose.words/editablerangestart/id/) { get; set; } | Especifica el identificador del rango editable. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Devuelve verdadero si este nodo puede contener otros nodos. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words/editablerangestart/nodetype/) { get; } | DevolucionesEditableRangeStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un **Rango** objeto que representa la parte de un documento que está contenido en este nodo. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words/editablerangestart/accept/)(DocumentVisitor) | Acepta un visitante. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicado del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtiene el primer ancestro del especificado[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtiene el primer ancestro del tipo de objeto especificado. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtiene el siguiente nodo de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtiene el nodo anterior de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina a sí mismo del padre. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporta el contenido del nodo a una cadena utilizando las opciones de guardado especificadas. |

### Observaciones

Un rango editable completo en un documento de Word consta de un[`EditableRangeStart`](./editablerangestart/) y una coincidencia[`EditableRangeEnd`](../editablerangeend/) con el mismo DNI.

[`EditableRangeStart`](./editablerangestart/) y[`EditableRangeEnd`](../editablerangeend/) son solo marcadores dentro de un documento que especifican dónde comienza y termina el rango editable.

Utilizar el[`EditableRange`](./editablerange/)class como una "fachada" para trabajar con un range editable como un solo objeto.

Actualmente, los rangos editables solo se admiten en el nivel en línea, es decir, dentro[`Paragraph`](../paragraph/), pero el inicio del rango editable y el final del rango editable pueden estar en párrafos diferentes.

### Ejemplos

Muestra cómo limitar los derechos de edición de rangos editables a un grupo/usuario específico.

```csharp
public void Visitor()
{
    Document doc = new Document();
    doc.Protect(ProtectionType.ReadOnly, "MyPassword");

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                    " we cannot edit this paragraph without the password.");

    // Cuando protegemos documentos contra escritura, los rangos editables nos permiten seleccionar áreas específicas que los usuarios pueden editar.
    // Hay dos formas mutuamente excluyentes de reducir la lista de editores permitidos.
    // 1 - Especifique un usuario:
    EditableRange editableRange = builder.StartEditableRange().EditableRange;
    editableRange.SingleUser = "john.doe@myoffice.com";
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.SingleUser}.");
    builder.EndEditableRange();

    Assert.AreEqual(EditorType.Unspecified, editableRange.EditorGroup);

    // 2 - Especifique un grupo con el que los usuarios permitidos estén asociados:
    editableRange = builder.StartEditableRange().EditableRange;
    editableRange.EditorGroup = EditorType.Administrators;
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.EditorGroup}.");
    builder.EndEditableRange();

    Assert.AreEqual(string.Empty, editableRange.SingleUser);

    builder.Writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

    // Imprimir detalles y contenidos de cada rango editable en el documento.
    EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

    doc.Accept(editableRangePrinter);

    Console.WriteLine(editableRangePrinter.ToText());
}

/// <summary>
/// Recopila las propiedades y el contenido de los rangos editables visitados en una cadena.
/// </summary>
public class EditableRangePrinter : DocumentVisitor
{
    public EditableRangePrinter()
    {
        mBuilder = new StringBuilder();
    }

    public string ToText()
    {
        return mBuilder.ToString();
    }

    public void Reset()
    {
        mBuilder.Clear();
        mInsideEditableRange = false;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo EditableRangeStart en el documento.
    /// </summary>
    public override VisitorAction VisitEditableRangeStart(EditableRangeStart editableRangeStart)
    {
        mBuilder.AppendLine(" -- Editable range found! -- ");
        mBuilder.AppendLine("\tID:\t\t" + editableRangeStart.Id);
        if (editableRangeStart.EditableRange.SingleUser == string.Empty)
            mBuilder.AppendLine("\tGroup:\t" + editableRangeStart.EditableRange.EditorGroup);
        else
            mBuilder.AppendLine("\tUser:\t" + editableRangeStart.EditableRange.SingleUser);
        mBuilder.AppendLine("\tContents:");

        mInsideEditableRange = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo EditableRangeEnd en el documento.
    /// </summary>
    public override VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
    {
        mBuilder.AppendLine(" -- End of editable range --\n");

        mInsideEditableRange = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo Ejecutar en el documento. Este visitante solo registra carreras que están dentro de rangos editables.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mInsideEditableRange) mBuilder.AppendLine("\t\"" + run.Text + "\"");

        return VisitorAction.Continue;
    }

    private bool mInsideEditableRange;
    private readonly StringBuilder mBuilder;
}
```

### Ver también

* class [Node](../node/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
