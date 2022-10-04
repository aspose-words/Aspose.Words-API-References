---
title: SingleUser
second_title: Referencia de API de Aspose.Words para .NET
description: Devuelve o establece el usuario único para el rango editable.
type: docs
weight: 50
url: /es/net/aspose.words/editablerange/singleuser/
---
## EditableRange.SingleUser property

Devuelve o establece el usuario único para el rango editable.

```csharp
public string SingleUser { get; set; }
```

### Observaciones

Este editor se puede almacenar en una de las siguientes formas:

DOMINIO\Nombre de usuario: para usuarios cuyo acceso se autenticará con las credenciales de dominio del usuario actual.

usuario@dominio.com: para usuarios cuyo acceso se autenticará utilizando la dirección de correo electrónico del usuario como credenciales.

usuario: para usuarios cuyo acceso se autenticará utilizando las credenciales de la máquina del usuario actual.

El usuario único y el grupo de editores no se pueden configurar simultáneamente para el rango editable específico, si uno está configurado, el otro estará claro.

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

* class [EditableRange](../)
* espacio de nombres [Aspose.Words](../../editablerange/)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
