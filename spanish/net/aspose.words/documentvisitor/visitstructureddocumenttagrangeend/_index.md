---
title: DocumentVisitor.VisitStructuredDocumentTagRangeEnd
linktitle: VisitStructuredDocumentTagRangeEnd
articleTitle: VisitStructuredDocumentTagRangeEnd
second_title: Aspose.Words para .NET
description: Descubra el método DocumentVisitor VisitStructuredDocumentTagRangeEnd, esencial para manejar etiquetas de documentos estructurados de manera efectiva en sus aplicaciones.
type: docs
weight: 450
url: /es/net/aspose.words/documentvisitor/visitstructureddocumenttagrangeend/
---
## DocumentVisitor.VisitStructuredDocumentTagRangeEnd method

Se llama cuando se encuentra un StructuredDocumentTagRangeEnd.

```csharp
public virtual VisitorAction VisitStructuredDocumentTagRangeEnd(
    StructuredDocumentTagRangeEnd sdtRangeEnd)
```

## Ejemplos

Muestra cómo utilizar un visitante de documentos para imprimir la estructura de nodos de un documento.

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // Cuando conseguimos que un nodo compuesto acepte un visitante de documento, el visitante visita el nodo que lo acepta,
    // y luego recorre todos los nodos secundarios en profundidad.
    //El visitante puede leer y modificar cada nodo visitado.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Recorre el árbol de nodos secundarios de un nodo.
/// Crea un mapa de este árbol en forma de cadena.
/// </summary>
public class DocStructurePrinter : DocumentVisitor
{
    public DocStructurePrinter()
    {
        mAcceptingNodeChildTree = new StringBuilder();
    }

    public string GetText()
    {
        return mAcceptingNodeChildTree.ToString();
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo de documento.
    /// </summary>
    public override VisitorAction VisitDocumentStart(Document doc)
    {
        int childNodeCount = doc.GetChildNodes(NodeType.Any, true).Count;

        IndentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
        mDocTraversalDepth++;

        // Permitir que el visitante continúe visitando otros nodos.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama después de que se hayan visitado todos los nodos secundarios de un nodo de Documento.
    /// </summary>
    public override VisitorAction VisitDocumentEnd(Document doc)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Document end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo de Sección en el documento.
    /// </summary>
    public override VisitorAction VisitSectionStart(Section section)
    {
        //Obtener el índice de nuestra sección dentro del documento.
        NodeCollection docSections = section.Document.GetChildNodes(NodeType.Section, false);
        int sectionIndex = docSections.IndexOf(section);

        IndentAndAppendLine("[Section start] Section index: " + sectionIndex);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama después de que se hayan visitado todos los nodos secundarios de un nodo de Sección.
    /// </summary>
    public override VisitorAction VisitSectionEnd(Section section)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Section end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo Cuerpo en el documento.
    /// </summary>
    public override VisitorAction VisitBodyStart(Body body)
    {
        int paragraphCount = body.Paragraphs.Count;
        IndentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama después de que se hayan visitado todos los nodos secundarios de un nodo Cuerpo.
    /// </summary>
    public override VisitorAction VisitBodyEnd(Body body)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Body end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo de párrafo en el documento.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        IndentAndAppendLine("[Paragraph start]");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama después de que se hayan visitado todos los nodos secundarios de un nodo de párrafo.
    /// </summary>
    public override VisitorAction VisitParagraphEnd(Paragraph paragraph)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Paragraph end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo Ejecutar en el documento.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo SubDocumento en el documento.
    /// </summary>
    public override VisitorAction VisitSubDocument(SubDocument subDocument)
    {
        IndentAndAppendLine("[SubDocument]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo SubDocumento en el documento.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
    {
        IndentAndAppendLine("[SdtRangeStart]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo SubDocumento en el documento.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
    {
        IndentAndAppendLine("[SdtRangeEnd]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Agrega una línea al StringBuilder y sangrala dependiendo de qué tan profundo se encuentre el visitante en el árbol del documento.
    /// </summary>
    /// <param name="texto"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mAcceptingNodeChildTree.Append("|  ");

        mAcceptingNodeChildTree.AppendLine(text);
    }

    private int mDocTraversalDepth;
    private readonly StringBuilder mAcceptingNodeChildTree;
}
```

### Ver también

* enum [VisitorAction](../../visitoraction/)
* class [StructuredDocumentTagRangeEnd](../../../aspose.words.markup/structureddocumenttagrangeend/)
* class [DocumentVisitor](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
