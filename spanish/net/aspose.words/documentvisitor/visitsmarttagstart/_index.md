---
title: DocumentVisitor.VisitSmartTagStart
linktitle: VisitSmartTagStart
articleTitle: VisitSmartTagStart
second_title: Aspose.Words para .NET
description: Descubra el método VisitSmartTagStart de DocumentVisitor, su clave para gestionar de manera eficiente la enumeración de etiquetas inteligentes y mejorar el procesamiento de documentos.
type: docs
weight: 420
url: /es/net/aspose.words/documentvisitor/visitsmarttagstart/
---
## DocumentVisitor.VisitSmartTagStart method

Se llama cuando se inicia la enumeración de una etiqueta inteligente.

```csharp
public virtual VisitorAction VisitSmartTagStart(SmartTag smartTag)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| smartTag | SmartTag | El objeto que se está visitando. |

### Valor_devuelto

A[`VisitorAction`](../../visitoraction/) valor que especifica cómo continuar la enumeración.

## Ejemplos

Muestra cómo imprimir la estructura de nodo de cada etiqueta inteligente en un documento.

```csharp
public void SmartTagToText()
{
    Document doc = new Document(MyDir + "Smart tags.doc");
    SmartTagStructurePrinter visitor = new SmartTagStructurePrinter();

    // Cuando conseguimos que un nodo compuesto acepte un visitante de documento, el visitante visita el nodo que lo acepta,
    // y luego recorre todos los nodos secundarios en profundidad.
    //El visitante puede leer y modificar cada nodo visitado.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Recorre el árbol no binario de nodos secundarios de un nodo.
/// Crea un mapa en forma de cadena de todos los nodos SmartTag encontrados y sus hijos.
/// </summary>
public class SmartTagStructurePrinter : DocumentVisitor
{
    public SmartTagStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideSmartTag = false;
    }

    /// <summary>
    /// Obtiene el texto simple del documento que fue acumulado por el visitante.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo Ejecutar en el documento.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideSmartTag) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo SmartTag en el documento.
    /// </summary>
    public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
    {
        IndentAndAppendLine("[SmartTag start] Name: " + smartTag.Element);
        mDocTraversalDepth++;
        mVisitorIsInsideSmartTag = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama después de que se hayan visitado todos los nodos secundarios de un nodo SmartTag.
    /// </summary>
    public override VisitorAction VisitSmartTagEnd(SmartTag smartTag)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[SmartTag end]");
        mVisitorIsInsideSmartTag = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Agrega una línea al StringBuilder y sangrala dependiendo de qué tan profundo se encuentre el visitante en el árbol del documento.
    /// </summary>
    /// <param name="texto"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideSmartTag;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Ver también

* enum [VisitorAction](../../visitoraction/)
* class [SmartTag](../../../aspose.words.markup/smarttag/)
* class [DocumentVisitor](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
