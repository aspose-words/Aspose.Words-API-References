---
title: EditableRange.EditorGroup
linktitle: EditorGroup
articleTitle: EditorGroup
second_title: Aspose.Words para .NET
description: Administre los permisos de usuario sin esfuerzo con la propiedad EditorGroup EditableRange, lo que permite controlar el acceso de edición para una mejor colaboración.
type: docs
weight: 30
url: /es/net/aspose.words/editablerange/editorgroup/
---
## EditableRange.EditorGroup property

Devuelve o establece un alias (o grupo de edición) que se utilizará para determinar si el usuario actual podrá editar este rango editable.

```csharp
public EditorType EditorGroup { get; set; }
```

## Observaciones

No es posible configurar un solo usuario y un grupo de editores simultáneamente para el rango editable específico; si se configura uno, el otro quedará claro.

## Ejemplos

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

//Actualmente, el cursor de inserción de nodo del generador de documentos se encuentra en más de un rango editable en curso.
// Cuando queremos finalizar un rango editable en esta situación,
// necesitamos especificar cuál de los rangos deseamos que finalice pasando su nodo EditableRangeStart.
builder.EndEditableRange(innerEditableRangeStart);

builder.Writeln("This paragraph inside the outer editable range and can be edited.");

builder.EndEditableRange(outerEditableRangeStart);

builder.Writeln("This paragraph is outside any editable ranges, and cannot be edited.");

// Si una región de texto tiene dos rangos editables superpuestos con grupos específicos,
//al grupo combinado de usuarios excluidos por ambos grupos se le impide editarlo.
outerEditableRangeStart.EditableRange.EditorGroup = EditorType.Everyone;
innerEditableRangeStart.EditableRange.EditorGroup = EditorType.Contributors;

doc.Save(ArtifactsDir + "EditableRange.Nested.docx");
```

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

* enum [EditorType](../../editortype/)
* class [EditableRange](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
