---
title: DocumentVisitor.VisitFieldStart
linktitle: VisitFieldStart
articleTitle: VisitFieldStart
second_title: Aspose.Words para .NET
description: Descubra el método DocumentVisitor VisitFieldStart, que se activa al comienzo de un campo en su documento, mejorando su eficiencia de codificación y su flujo de trabajo.
type: docs
weight: 200
url: /es/net/aspose.words/documentvisitor/visitfieldstart/
---
## DocumentVisitor.VisitFieldStart method

Se llama cuando un campo comienza en el documento.

```csharp
public virtual VisitorAction VisitFieldStart(FieldStart fieldStart)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fieldStart | FieldStart | El objeto que se está visitando. |

### Valor_devuelto

A[`VisitorAction`](../../visitoraction/) valor que especifica cómo continuar la enumeración.

## Observaciones

Un campo en un documento de Word consta de un código de campo y un valor de campo.

Por ejemplo, un campo que muestra un número de página se puede representar de la siguiente manera:

[Inicio de campo]PÁGINA[Separador de campo]98[Fin de campo]

El separador de campo separa el código del valor del campo en el documento. Tenga en cuenta que algunos campos solo tienen código de campo y no tienen separador ni valor de campo.

Los campos se pueden anidar.

## Ejemplos

Muestra cómo imprimir la estructura de nodos de cada campo de un documento.

```csharp
public void FieldToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    FieldStructurePrinter visitor = new FieldStructurePrinter();

    // Cuando conseguimos que un nodo compuesto acepte un visitante de documento, el visitante visita el nodo que lo acepta,
    // y luego recorre todos los nodos secundarios en profundidad.
    //El visitante puede leer y modificar cada nodo visitado.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Recorre el árbol no binario de nodos secundarios de un nodo.
/// Crea un mapa en forma de cadena de todos los nodos de campo encontrados y sus hijos.
/// </summary>
public class FieldStructurePrinter : DocumentVisitor
{
    public FieldStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideField = false;
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo Ejecutar en el documento.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideField) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo FieldStart en el documento.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        IndentAndAppendLine("[Field start] FieldType: " + fieldStart.FieldType);
        mDocTraversalDepth++;
        mVisitorIsInsideField = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo FieldEnd en el documento.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Field end]");
        mVisitorIsInsideField = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo FieldSeparator en el documento.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        IndentAndAppendLine("[FieldSeparator]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Agrega una línea al StringBuilder y sangra según la profundidad del visitante
    /// en el árbol de nodos secundarios del campo.
    /// </summary>
    /// <param name="texto"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++)
        {
            mBuilder.Append("|  ");
        }

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideField;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Ver también

* enum [VisitorAction](../../visitoraction/)
* class [FieldStart](../../../aspose.words.fields/fieldstart/)
* class [DocumentVisitor](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
