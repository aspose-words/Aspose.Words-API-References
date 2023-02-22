---
title: DocumentVisitor.VisitEditableRangeEnd
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentVisitor método. Llamado cuando se encuentra el final de un rango editable en el documento.
type: docs
weight: 160
url: /es/net/aspose.words/documentvisitor/visiteditablerangeend/
---
## DocumentVisitor.VisitEditableRangeEnd method

Llamado cuando se encuentra el final de un rango editable en el documento.

```csharp
public virtual VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| editableRangeEnd | EditableRangeEnd | El objeto que se está visitando. |

### Valor_devuelto

A[`VisitorAction`](../../visitoraction/) valor que especifica cómo continuar la enumeración.

### Ejemplos

Muestra cómo imprimir la estructura de nodos de cada rango editable en un documento.

```csharp
public void EditableRangeToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    EditableRangeStructurePrinter visitor = new EditableRangeStructurePrinter();

    // Cuando conseguimos que un nodo compuesto acepte un documento visitante, el visitante visita el nodo de aceptación,
    // y luego atraviesa todos los elementos secundarios del nodo en profundidad.
    // El visitante puede leer y modificar cada nodo visitado.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Atraviesa el árbol no binario de nodos secundarios de un nodo.
/// Crea un mapa en forma de cadena de todos los nodos EditableRange encontrados y sus hijos.
/// </summary>
public class EditableRangeStructurePrinter : DocumentVisitor
{
    public EditableRangeStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideEditableRange = false;
    }

    /// <summary>
    /// Obtiene el texto sin formato del documento que fue acumulado por el visitante.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo Ejecutar en el documento.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        // Queremos imprimir el contenido de las ejecuciones, pero solo si están dentro de las formas, como sería en el caso de los cuadros de texto.
        if (mVisitorIsInsideEditableRange) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo EditableRange en el documento.
    /// </summary>
    public override VisitorAction VisitEditableRangeStart(EditableRangeStart editableRangeStart)
    {
        IndentAndAppendLine("[EditableRange start] ID: " + editableRangeStart.Id + " Owner: " +
                            editableRangeStart.EditableRange.SingleUser);
        mDocTraversalDepth++;
        mVisitorIsInsideEditableRange = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando finaliza la visita de un nodo EditableRange.
    /// </summary>
    public override VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[EditableRange end]");
        mVisitorIsInsideEditableRange = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Agregue una línea al StringBuilder y sangre dependiendo de qué tan profundo esté el visitante en el árbol del documento.
    /// </summary>
    /// <parámetro nombre="texto"></parámetro>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideEditableRange;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Ver también

* enum [VisitorAction](../../visitoraction/)
* class [EditableRangeEnd](../../editablerangeend/)
* class [DocumentVisitor](../)
* espacio de nombres [Aspose.Words](../../documentvisitor/)
* asamblea [Aspose.Words](../../../)


