---
title: Class DocumentVisitor
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.DocumentVisitor clase. Clase base para visitantes de documentos personalizados.
type: docs
weight: 470
url: /es/net/aspose.words/documentvisitor/
---
## DocumentVisitor class

Clase base para visitantes de documentos personalizados.

Para obtener más información, visite el[Modelo de objetos de documento (DOM) de Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) artículo de documentación.

```csharp
public abstract class DocumentVisitor
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| virtual [VisitAbsolutePositionTab](../../aspose.words/documentvisitor/visitabsolutepositiontab/)(AbsolutePositionTab) | Llamado cuando un[`AbsolutePositionTab`](../absolutepositiontab/) Se encuentra un nodo en el documento. |
| virtual [VisitBodyEnd](../../aspose.words/documentvisitor/visitbodyend/)(Body) | Se llama cuando finaliza la enumeración de la historia del texto principal en una sección. |
| virtual [VisitBodyStart](../../aspose.words/documentvisitor/visitbodystart/)(Body) | Se llama cuando ha comenzado la enumeración de la historia del texto principal en una sección. |
| virtual [VisitBookmarkEnd](../../aspose.words/documentvisitor/visitbookmarkend/)(BookmarkEnd) | Se llama cuando se encuentra el final de un marcador en el documento. |
| virtual [VisitBookmarkStart](../../aspose.words/documentvisitor/visitbookmarkstart/)(BookmarkStart) | Se llama cuando se encuentra el inicio de un marcador en el documento. |
| virtual [VisitBuildingBlockEnd](../../aspose.words/documentvisitor/visitbuildingblockend/)(BuildingBlock) | Se llama cuando finaliza la enumeración de un bloque de construcción. |
| virtual [VisitBuildingBlockStart](../../aspose.words/documentvisitor/visitbuildingblockstart/)(BuildingBlock) | Se llama cuando ha comenzado la enumeración de un bloque de construcción. |
| virtual [VisitCellEnd](../../aspose.words/documentvisitor/visitcellend/)(Cell) | Se llama cuando finaliza la enumeración de una celda de la tabla. |
| virtual [VisitCellStart](../../aspose.words/documentvisitor/visitcellstart/)(Cell) | Se llama cuando ha comenzado la enumeración de una celda de la tabla. |
| virtual [VisitCommentEnd](../../aspose.words/documentvisitor/visitcommentend/)(Comment) | Se llama cuando finaliza la enumeración de un texto de comentario. |
| virtual [VisitCommentRangeEnd](../../aspose.words/documentvisitor/visitcommentrangeend/)(CommentRangeEnd) | Se llama cuando se encuentra el final de un rango de texto comentado. |
| virtual [VisitCommentRangeStart](../../aspose.words/documentvisitor/visitcommentrangestart/)(CommentRangeStart) | Se llama cuando se encuentra el inicio de un rango de texto comentado. |
| virtual [VisitCommentStart](../../aspose.words/documentvisitor/visitcommentstart/)(Comment) | Se llama cuando ha comenzado la enumeración de un texto de comentario. |
| virtual [VisitDocumentEnd](../../aspose.words/documentvisitor/visitdocumentend/)(Document) | Se llama cuando finaliza la enumeración del documento. |
| virtual [VisitDocumentStart](../../aspose.words/documentvisitor/visitdocumentstart/)(Document) | Se llama cuando ha comenzado la enumeración del documento. |
| virtual [VisitEditableRangeEnd](../../aspose.words/documentvisitor/visiteditablerangeend/)(EditableRangeEnd) | Se llama cuando se encuentra el final de un rango editable en el documento. |
| virtual [VisitEditableRangeStart](../../aspose.words/documentvisitor/visiteditablerangestart/)(EditableRangeStart) | Se llama cuando se encuentra el inicio de un rango editable en el documento. |
| virtual [VisitFieldEnd](../../aspose.words/documentvisitor/visitfieldend/)(FieldEnd) | Se llama cuando un campo termina en el documento. |
| virtual [VisitFieldSeparator](../../aspose.words/documentvisitor/visitfieldseparator/)(FieldSeparator) | Se llama cuando se encuentra un separador de campo en el documento. |
| virtual [VisitFieldStart](../../aspose.words/documentvisitor/visitfieldstart/)(FieldStart) | Se llama cuando comienza un campo en el documento. |
| virtual [VisitFootnoteEnd](../../aspose.words/documentvisitor/visitfootnoteend/)(Footnote) | Se llama cuando finaliza la enumeración de una nota al pie o del texto de una nota al final. |
| virtual [VisitFootnoteStart](../../aspose.words/documentvisitor/visitfootnotestart/)(Footnote) | Se llama cuando ha comenzado la enumeración de una nota al pie o del texto de una nota al final. |
| virtual [VisitFormField](../../aspose.words/documentvisitor/visitformfield/)(FormField) | Se llama cuando se encuentra un campo de formulario en el documento. |
| virtual [VisitGlossaryDocumentEnd](../../aspose.words/documentvisitor/visitglossarydocumentend/)(GlossaryDocument) | Se llama cuando finaliza la enumeración de un documento de glosario. |
| virtual [VisitGlossaryDocumentStart](../../aspose.words/documentvisitor/visitglossarydocumentstart/)(GlossaryDocument) | Se llama cuando ha comenzado la enumeración de un documento de glosario. |
| virtual [VisitGroupShapeEnd](../../aspose.words/documentvisitor/visitgroupshapeend/)(GroupShape) | Se llama cuando finaliza la enumeración de una forma de grupo. |
| virtual [VisitGroupShapeStart](../../aspose.words/documentvisitor/visitgroupshapestart/)(GroupShape) | Se llama cuando ha comenzado la enumeración de una forma de grupo. |
| virtual [VisitHeaderFooterEnd](../../aspose.words/documentvisitor/visitheaderfooterend/)(HeaderFooter) | Se llama cuando finaliza la enumeración de un encabezado o pie de página en una sección. |
| virtual [VisitHeaderFooterStart](../../aspose.words/documentvisitor/visitheaderfooterstart/)(HeaderFooter) | Se llama cuando ha comenzado la enumeración de un encabezado o pie de página en una sección. |
| virtual [VisitOfficeMathEnd](../../aspose.words/documentvisitor/visitofficemathend/)(OfficeMath) | Se llama cuando finaliza la enumeración de un objeto de Office Math. |
| virtual [VisitOfficeMathStart](../../aspose.words/documentvisitor/visitofficemathstart/)(OfficeMath) | Se llama cuando ha comenzado la enumeración de un objeto de Office Math. |
| virtual [VisitParagraphEnd](../../aspose.words/documentvisitor/visitparagraphend/)(Paragraph) | Se llama cuando finaliza la enumeración de un párrafo. |
| virtual [VisitParagraphStart](../../aspose.words/documentvisitor/visitparagraphstart/)(Paragraph) | Se llama cuando ha comenzado la enumeración de un párrafo. |
| virtual [VisitRowEnd](../../aspose.words/documentvisitor/visitrowend/)(Row) | Se llama cuando finaliza la enumeración de una fila de la tabla. |
| virtual [VisitRowStart](../../aspose.words/documentvisitor/visitrowstart/)(Row) | Se llama cuando ha comenzado la enumeración de una fila de la tabla. |
| virtual [VisitRun](../../aspose.words/documentvisitor/visitrun/)(Run) | Se llama cuando se encuentra una serie de texto en el. |
| virtual [VisitSectionEnd](../../aspose.words/documentvisitor/visitsectionend/)(Section) | Se llama cuando finaliza la enumeración de una sección. |
| virtual [VisitSectionStart](../../aspose.words/documentvisitor/visitsectionstart/)(Section) | Se llama cuando ha comenzado la enumeración de una sección. |
| virtual [VisitShapeEnd](../../aspose.words/documentvisitor/visitshapeend/)(Shape) | Se llama cuando finaliza la enumeración de una forma. |
| virtual [VisitShapeStart](../../aspose.words/documentvisitor/visitshapestart/)(Shape) | Se llama cuando ha comenzado la enumeración de una forma. |
| virtual [VisitSmartTagEnd](../../aspose.words/documentvisitor/visitsmarttagend/)(SmartTag) | Se llama cuando finaliza la enumeración de una etiqueta inteligente. |
| virtual [VisitSmartTagStart](../../aspose.words/documentvisitor/visitsmarttagstart/)(SmartTag) | Se llama cuando ha comenzado la enumeración de una etiqueta inteligente. |
| virtual [VisitSpecialChar](../../aspose.words/documentvisitor/visitspecialchar/)(SpecialChar) | Llamado cuando un[`SpecialChar`](../specialchar/) Se encuentra un nodo en el documento. |
| virtual [VisitStructuredDocumentTagEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagend/)(StructuredDocumentTag) | Se llama cuando finaliza la enumeración de una etiqueta de documento estructurado. |
| virtual [VisitStructuredDocumentTagRangeEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagrangeend/)(StructuredDocumentTagRangeEnd) | Se llama cuando se encuentra StructuredDocumentTagRangeEnd. |
| virtual [VisitStructuredDocumentTagRangeStart](../../aspose.words/documentvisitor/visitstructureddocumenttagrangestart/)(StructuredDocumentTagRangeStart) | Se llama cuando se encuentra StructuredDocumentTagRangeStart. |
| virtual [VisitStructuredDocumentTagStart](../../aspose.words/documentvisitor/visitstructureddocumenttagstart/)(StructuredDocumentTag) | Se llama cuando ha comenzado la enumeración de una etiqueta de documento estructurado. |
| virtual [VisitSubDocument](../../aspose.words/documentvisitor/visitsubdocument/)(SubDocument) | Se llama cuando se encuentra un subdocumento. |
| virtual [VisitTableEnd](../../aspose.words/documentvisitor/visittableend/)(Table) | Se llama cuando finaliza la enumeración de una tabla. |
| virtual [VisitTableStart](../../aspose.words/documentvisitor/visittablestart/)(Table) | Se llama cuando ha comenzado la enumeración de una tabla. |

### Observaciones

Con`DocumentVisitor` puede definir y ejecutar operaciones personalizadas que requieren enumeración en el árbol del documento.

Por ejemplo, Aspose.Words usa`DocumentVisitor` internamente para guardar[`Document`](../document/) en varios formatos y para otras operaciones como buscar campos o marcadores sobre un fragmento de un documento.

Usar`DocumentVisitor`:

1. Crear una clase derivada de`DocumentVisitor`.
2. Anule y proporcione implementaciones para algunos o todos los métodos de VisitXXX para realizar algunas operaciones personalizadas.
3. Llamar[`Nodo.Aceptar`](../node/accept/) sobre el[`Node`](../node/) that desde donde desea iniciar la enumeración.

`DocumentVisitor` proporciona implementaciones predeterminadas para todos los métodos de VisitXXX para facilitar la creación de nuevos visitantes de documentos, ya que solo es necesario anular los métodos necesarios para el visitante particular. No es necesario anular todos los métodos de visitante.

Para obtener más información, consulte el patrón de diseño de visitante.

### Ejemplos

Muestra cómo utilizar un visitante de documentos para imprimir la estructura de nodos de un documento.

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // Cuando conseguimos que un nodo compuesto acepte un visitante del documento, el visitante visita el nodo receptor,
    // y luego atraviesa todos los hijos del nodo en profundidad.
    // El visitante puede leer y modificar cada nodo visitado.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Atraviesa el árbol de nodos secundarios de un nodo.
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
    /// Se llama cuando se encuentra un nodo Documento.
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
    /// Se llama después de que se hayan visitado todos los nodos secundarios de un nodo de documento.
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
        // Obtener el índice de nuestra sección dentro del documento.
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
    /// Se llama después de que se hayan visitado todos los nodos secundarios de un nodo Body.
    /// </summary>
    public override VisitorAction VisitBodyEnd(Body body)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Body end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo Párrafo en el documento.
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
    /// Agrega una línea al StringBuilder y sangra dependiendo de qué tan profundo esté el visitante en el árbol del documento.
    /// </summary>
    /// <param nombre="texto"></param>
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

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


