---
title: Accept
second_title: Referencia de API de Aspose.Words para .NET
description: Acepta un visitante.
type: docs
weight: 350
url: /es/net/aspose.words.tables/table/accept/
---
## Table.Accept method

Acepta un visitante.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| visitor | DocumentVisitor | El visitante que visitará los nodos. |

### Valor_devuelto

True si se visitaron todos los nodos; false si DocumentVisitor detuvo la operación antes de visitar todos los nodos.

### Observaciones

Enumera sobre este nodo y todos sus hijos. Cada nodo llama a un método correspondiente en DocumentVisitor.

Para obtener más información, consulte el patrón de diseño Visitante.

Llama a DocumentVisitor.VisitTableStart, luego llama a Accept para todos los nodos secundarios de la sección y llama a DocumentVisitor.VisitTableEnd al final.

### Ejemplos

Muestra cómo usar una implementación de DocumentVisitor para eliminar todo el contenido oculto de un documento.

```csharp
{
    Document doc = new Document(MyDir + "Hidden content.docx");

    RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

    // A continuación hay tres tipos de campos que pueden aceptar un visitante del documento,
    // lo que le permitirá visitar el nodo de aceptación y luego atravesar sus nodos secundarios en profundidad.
    // 1 - Nodo de párrafo:
    Paragraph para = (Paragraph) doc.GetChild(NodeType.Paragraph, 4, true);
    para.Accept(hiddenContentRemover);

    // 2 - Nodo de tabla:
    Table table = doc.FirstSection.Body.Tables[0];
    table.Accept(hiddenContentRemover);

    // 3 - Nodo de documento:
    doc.Accept(hiddenContentRemover);

    doc.Save(ArtifactsDir + "Font.RemoveHiddenContentFromDocument.docx");

/// <summary>
/// Elimina todos los nodos visitados marcados como "contenido oculto".
/// </summary>
public class RemoveHiddenContentVisitor : DocumentVisitor
{
    /// <summary>
    /// Llamado cuando se encuentra un nodo FieldStart en el documento.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        if (fieldStart.Font.Hidden)
            fieldStart.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo FieldEnd en el documento.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.Font.Hidden)
            fieldEnd.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo FieldSeparator en el documento.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        if (fieldSeparator.Font.Hidden)
            fieldSeparator.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo Ejecutar en el documento.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (run.Font.Hidden)
            run.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo de párrafo en el documento.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        if (paragraph.ParagraphBreakFont.Hidden)
            paragraph.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un FormField en el documento.
    /// </summary>
    public override VisitorAction VisitFormField(FormField formField)
    {
        if (formField.Font.Hidden)
            formField.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un GroupShape en el documento.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        if (groupShape.Font.Hidden)
            groupShape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra una Forma en el documento.
    /// </summary>
    public override VisitorAction VisitShapeStart(Shape shape)
    {
        if (shape.Font.Hidden)
            shape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un comentario en el documento.
    /// </summary>
    public override VisitorAction VisitCommentStart(Comment comment)
    {
        if (comment.Font.Hidden)
            comment.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra una nota al pie en el documento.
    /// </summary>
    public override VisitorAction VisitFootnoteStart(Footnote footnote)
    {
        if (footnote.Font.Hidden)
            footnote.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un carácter especial en el documento.
    /// </summary>
    public override VisitorAction VisitSpecialChar(SpecialChar specialChar)
    {
        if (specialChar.Font.Hidden)
            specialChar.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se finaliza la visita de un nodo Tabla en el documento.
    /// </summary>
    public override VisitorAction VisitTableEnd(Table table)
    {
        // El contenido dentro de las celdas de la tabla puede tener el indicador de contenido oculto, pero las tablas en sí no pueden.
        // Si esta tabla no tuviera nada más que contenido oculto, este visitante lo habría eliminado todo,
        // y no quedarían nodos secundarios.
        // Por lo tanto, también podemos tratar la tabla en sí misma como contenido oculto y eliminarla.
        // Las tablas que están vacías pero no tienen contenido oculto tendrán celdas con párrafos vacíos dentro,
        // que este visitante no eliminará.
        if (!table.HasChildNodes)
            table.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se finaliza la visita de un nodo Cell en el documento.
    /// </summary>
    public override VisitorAction VisitCellEnd(Cell cell)
    {
        if (!cell.HasChildNodes && cell.ParentNode != null)
            cell.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando finaliza la visita de un nodo Fila en el documento.
    /// </summary>
    public override VisitorAction VisitRowEnd(Row row)
    {
        if (!row.HasChildNodes && row.ParentNode != null)
            row.Remove();

        return VisitorAction.Continue;
    }
}
```

### Ver también

* class [DocumentVisitor](../../../aspose.words/documentvisitor)
* class [Table](../../table)
* espacio de nombres [Aspose.Words.Tables](../../table)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
