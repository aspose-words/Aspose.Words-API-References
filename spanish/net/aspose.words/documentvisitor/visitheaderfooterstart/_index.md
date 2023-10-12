---
title: DocumentVisitor.VisitHeaderFooterStart
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentVisitor método. Se llama cuando ha comenzado la enumeración de un encabezado o pie de página en una sección.
type: docs
weight: 290
url: /es/net/aspose.words/documentvisitor/visitheaderfooterstart/
---
## DocumentVisitor.VisitHeaderFooterStart method

Se llama cuando ha comenzado la enumeración de un encabezado o pie de página en una sección.

```csharp
public virtual VisitorAction VisitHeaderFooterStart(HeaderFooter headerFooter)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| headerFooter | HeaderFooter | El objeto que se está visitando. |

### Valor_devuelto

A[`VisitorAction`](../../visitoraction/) valor que especifica cómo continuar la enumeración.

### Ejemplos

Muestra cómo imprimir la estructura de nodos de cada encabezado y pie de página de un documento.

```csharp
public void HeaderFooterToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    HeaderFooterStructurePrinter visitor = new HeaderFooterStructurePrinter();

    // Cuando conseguimos que un nodo compuesto acepte un visitante del documento, el visitante visita el nodo receptor,
    // y luego atraviesa todos los hijos del nodo en profundidad.
    // El visitante puede leer y modificar cada nodo visitado.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // Una forma alternativa de acceder al encabezado/pie de página de un documento sección por sección es accediendo a la colección.
    HeaderFooter[] headerFooters = doc.FirstSection.HeadersFooters.ToArray();
    Assert.AreEqual(3, headerFooters.Length);
}

/// <summary>
/// Atraviesa el árbol no binario de nodos secundarios de un nodo.
/// Crea un mapa en forma de cadena de todos los nodos HeaderFooter encontrados y sus hijos.
/// </summary>
public class HeaderFooterStructurePrinter : DocumentVisitor
{
    public HeaderFooterStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideHeaderFooter = false;
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
        if (mVisitorIsInsideHeaderFooter) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo HeaderFooter en el documento.
    /// </summary>
    public override VisitorAction VisitHeaderFooterStart(HeaderFooter headerFooter)
    {
        IndentAndAppendLine("[HeaderFooter start] HeaderFooterType: " + headerFooter.HeaderFooterType);
        mDocTraversalDepth++;
        mVisitorIsInsideHeaderFooter = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama después de que se hayan visitado todos los nodos secundarios de un nodo HeaderFooter.
    /// </summary>
    public override VisitorAction VisitHeaderFooterEnd(HeaderFooter headerFooter)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[HeaderFooter end]");
        mVisitorIsInsideHeaderFooter = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Agrega una línea al StringBuilder y sangra dependiendo de qué tan profundo esté el visitante en el árbol del documento.
    /// </summary>
    /// <param nombre="texto"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideHeaderFooter;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Ver también

* enum [VisitorAction](../../visitoraction/)
* class [HeaderFooter](../../headerfooter/)
* class [DocumentVisitor](../)
* espacio de nombres [Aspose.Words](../../documentvisitor/)
* asamblea [Aspose.Words](../../../)


