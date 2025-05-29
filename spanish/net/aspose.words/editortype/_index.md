---
title: EditorType Enum
linktitle: EditorType
articleTitle: EditorType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.EditorType, que define grupos de edición para controlar los permisos de usuario para la edición de rangos de documentos. ¡Mejore su gestión documental hoy mismo!
type: docs
weight: 1860
url: /es/net/aspose.words/editortype/
---
## EditorType enumeration

Especifica el conjunto de posibles alias (o grupos de edición) que se pueden usar como alias para determinar si se permitirá al usuario actual editar un único rango definido por un rango editable dentro de un documento.

```csharp
public enum EditorType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Unspecified | `0` | Significa que no se especificó el tipo de editor. |
| Administrators | `1` | Especifica que los usuarios asociados con el grupo Administradores podrán editar rangos editables utilizando este tipo de edición cuando la protección del documento esté habilitada. |
| Contributors | `2` | Especifica que a los usuarios asociados con el grupo Colaboradores se les permitirá editar rangos editables usando este tipo de edición cuando la protección del documento esté habilitada. |
| Current | `3` | Especifica que los usuarios asociados con el grupo Actual podrán editar rangos editables usando este tipo de edición cuando la protección del documento esté habilitada. |
| Editors | `4` | Especifica que los usuarios asociados con el grupo Editores podrán editar rangos editables usando este tipo de edición cuando la protección del documento esté habilitada. |
| Everyone | `5` | Especifica que todos los usuarios que abren el documento podrán editar rangos editables usando este tipo de edición cuando la protección del documento esté habilitada. |
| None | `6` | Especifica que ninguno de los usuarios que abren el documento podrá editar rangos editables utilizando este tipo de edición cuando la protección del documento esté habilitada. |
| Owners | `7` | Especifica que los usuarios asociados con el grupo Propietarios podrán editar rangos editables usando este tipo de edición cuando la protección del documento esté habilitada. |
| Default | `0` | Lo mismo queUnspecified . |

## Ejemplos

Muestra cómo limitar los derechos de edición de rangos editables a un grupo/usuario específico.

```csharp
public void Visitor()
{
    Document doc = new Document();
    doc.Protect(ProtectionType.ReadOnly, "MyPassword");

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                    " we cannot edit this paragraph without the password.");

    // Cuando protegemos contra escritura documentos, los rangos editables nos permiten elegir áreas específicas que los usuarios pueden editar.
    // Hay dos formas mutuamente excluyentes de limitar la lista de editores permitidos.
    // 1 - Especifica un usuario:
    EditableRange editableRange = builder.StartEditableRange().EditableRange;
    editableRange.SingleUser = "john.doe@myoffice.com";
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.SingleUser}.");
    builder.EndEditableRange();

    Assert.AreEqual(EditorType.Unspecified, editableRange.EditorGroup);

    // 2 - Especifique un grupo al que se asocien los usuarios permitidos:
    editableRange = builder.StartEditableRange().EditableRange;
    editableRange.EditorGroup = EditorType.Administrators;
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.EditorGroup}.");
    builder.EndEditableRange();

    Assert.AreEqual(string.Empty, editableRange.SingleUser);

    builder.Writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

    // Imprima detalles y contenidos de cada rango editable en el documento.
    EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

    doc.Accept(editableRangePrinter);

    Console.WriteLine(editableRangePrinter.ToText());
}

/// <summary>
/// Recopila propiedades y contenidos de los rangos editables visitados en una cadena.
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
    /// Se llama cuando se encuentra un nodo EditableRangeStart en el documento.
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
    /// Se llama cuando se encuentra un nodo EditableRangeEnd en el documento.
    /// </summary>
    public override VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
    {
        mBuilder.AppendLine(" -- End of editable range --\n");

        mInsideEditableRange = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    Se llama cuando se encuentra un nodo de ejecución en el documento. Este visitante solo registra las ejecuciones dentro de los rangos editables.
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

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
