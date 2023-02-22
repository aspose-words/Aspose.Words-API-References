---
title: Class DocumentVisitor
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.DocumentVisitor clase. Clase base para visitantes de documentos personalizados.
type: docs
weight: 460
url: /es/net/aspose.words/documentvisitor/
---
## DocumentVisitor class

Clase base para visitantes de documentos personalizados.

```csharp
public abstract class DocumentVisitor
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| virtual [VisitAbsolutePositionTab](../../aspose.words/documentvisitor/visitabsolutepositiontab/)(AbsolutePositionTab) | Llamado cuando un[`AbsolutePositionTab`](../absolutepositiontab/) nodo se encuentra en el documento. |
| virtual [VisitBodyEnd](../../aspose.words/documentvisitor/visitbodyend/)(Body) | Se llama cuando finaliza la enumeración del artículo de texto principal en una sección. |
| virtual [VisitBodyStart](../../aspose.words/documentvisitor/visitbodystart/)(Body) | Llamado cuando se ha iniciado la enumeración del artículo de texto principal en una sección. |
| virtual [VisitBookmarkEnd](../../aspose.words/documentvisitor/visitbookmarkend/)(BookmarkEnd) | Llamado cuando se encuentra el final de un marcador en el documento. |
| virtual [VisitBookmarkStart](../../aspose.words/documentvisitor/visitbookmarkstart/)(BookmarkStart) | Se llama cuando se encuentra el inicio de un marcador en el documento. |
| virtual [VisitBuildingBlockEnd](../../aspose.words/documentvisitor/visitbuildingblockend/)(BuildingBlock) | Se llama cuando finaliza la enumeración de un bloque de creación. |
| virtual [VisitBuildingBlockStart](../../aspose.words/documentvisitor/visitbuildingblockstart/)(BuildingBlock) | Llamado cuando ha comenzado la enumeración de un bloque de creación. |
| virtual [VisitCellEnd](../../aspose.words/documentvisitor/visitcellend/)(Cell) | Se llama cuando finaliza la enumeración de una celda de la tabla. |
| virtual [VisitCellStart](../../aspose.words/documentvisitor/visitcellstart/)(Cell) | Llamado cuando se ha iniciado la enumeración de una celda de la tabla. |
| virtual [VisitCommentEnd](../../aspose.words/documentvisitor/visitcommentend/)(Comment) | Se llama cuando finaliza la enumeración de un texto de comentario. |
| virtual [VisitCommentRangeEnd](../../aspose.words/documentvisitor/visitcommentrangeend/)(CommentRangeEnd) | Llamado cuando se encuentra el final de un rango de texto comentado. |
| virtual [VisitCommentRangeStart](../../aspose.words/documentvisitor/visitcommentrangestart/)(CommentRangeStart) | Llamado cuando se encuentra el inicio de un rango de texto comentado. |
| virtual [VisitCommentStart](../../aspose.words/documentvisitor/visitcommentstart/)(Comment) | Llamado cuando ha comenzado la enumeración de un texto de comentario. |
| virtual [VisitDocumentEnd](../../aspose.words/documentvisitor/visitdocumentend/)(Document) | Llamado cuando finaliza la enumeración del documento. |
| virtual [VisitDocumentStart](../../aspose.words/documentvisitor/visitdocumentstart/)(Document) | Llamado cuando ha comenzado la enumeración del documento. |
| virtual [VisitEditableRangeEnd](../../aspose.words/documentvisitor/visiteditablerangeend/)(EditableRangeEnd) | Llamado cuando se encuentra el final de un rango editable en el documento. |
| virtual [VisitEditableRangeStart](../../aspose.words/documentvisitor/visiteditablerangestart/)(EditableRangeStart) | Llamado cuando se encuentra un inicio de un rango editable en el documento. |
| virtual [VisitFieldEnd](../../aspose.words/documentvisitor/visitfieldend/)(FieldEnd) | Llamado cuando un campo termina en el documento. |
| virtual [VisitFieldSeparator](../../aspose.words/documentvisitor/visitfieldseparator/)(FieldSeparator) | Llamado cuando se encuentra un separador de campo en el documento. |
| virtual [VisitFieldStart](../../aspose.words/documentvisitor/visitfieldstart/)(FieldStart) | Llamado cuando un campo comienza en el documento. |
| virtual [VisitFootnoteEnd](../../aspose.words/documentvisitor/visitfootnoteend/)(Footnote) | Se llama cuando finaliza la enumeración del texto de una nota al pie o al final. |
| virtual [VisitFootnoteStart](../../aspose.words/documentvisitor/visitfootnotestart/)(Footnote) | Llamado cuando ha comenzado la enumeración de una nota al pie o al final del texto. |
| virtual [VisitFormField](../../aspose.words/documentvisitor/visitformfield/)(FormField) | Llamado cuando se encuentra un campo de formulario en el documento. |
| virtual [VisitGlossaryDocumentEnd](../../aspose.words/documentvisitor/visitglossarydocumentend/)(GlossaryDocument) | Se llama cuando finaliza la enumeración de un documento de glosario. |
| virtual [VisitGlossaryDocumentStart](../../aspose.words/documentvisitor/visitglossarydocumentstart/)(GlossaryDocument) | Llamado cuando se ha iniciado la enumeración de un documento de glosario. |
| virtual [VisitGroupShapeEnd](../../aspose.words/documentvisitor/visitgroupshapeend/)(GroupShape) | Se llama cuando finaliza la enumeración de una forma de grupo. |
| virtual [VisitGroupShapeStart](../../aspose.words/documentvisitor/visitgroupshapestart/)(GroupShape) | Llamado cuando ha comenzado la enumeración de una forma de grupo. |
| virtual [VisitHeaderFooterEnd](../../aspose.words/documentvisitor/visitheaderfooterend/)(HeaderFooter) | Se llama cuando finaliza la enumeración de un encabezado o pie de página en una sección. |
| virtual [VisitHeaderFooterStart](../../aspose.words/documentvisitor/visitheaderfooterstart/)(HeaderFooter) | Llamado cuando ha comenzado la enumeración de un encabezado o pie de página en una sección. |
| virtual [VisitOfficeMathEnd](../../aspose.words/documentvisitor/visitofficemathend/)(OfficeMath) | Llamado cuando finaliza la enumeración de un objeto Office Math. |
| virtual [VisitOfficeMathStart](../../aspose.words/documentvisitor/visitofficemathstart/)(OfficeMath) | Llamado cuando se ha iniciado la enumeración de un objeto Office Math. |
| virtual [VisitParagraphEnd](../../aspose.words/documentvisitor/visitparagraphend/)(Paragraph) | Llamado cuando finaliza la enumeración de un párrafo. |
| virtual [VisitParagraphStart](../../aspose.words/documentvisitor/visitparagraphstart/)(Paragraph) | Llamado cuando ha comenzado la enumeración de un párrafo. |
| virtual [VisitRowEnd](../../aspose.words/documentvisitor/visitrowend/)(Row) | Llamado cuando finaliza la enumeración de una fila de la tabla. |
| virtual [VisitRowStart](../../aspose.words/documentvisitor/visitrowstart/)(Row) | Llamado cuando ha comenzado la enumeración de una fila de la tabla. |
| virtual [VisitRun](../../aspose.words/documentvisitor/visitrun/)(Run) | Llamado cuando se encuentra una secuencia de texto en el. |
| virtual [VisitSectionEnd](../../aspose.words/documentvisitor/visitsectionend/)(Section) | Llamado cuando finaliza la enumeración de una sección. |
| virtual [VisitSectionStart](../../aspose.words/documentvisitor/visitsectionstart/)(Section) | Llamado cuando se ha iniciado la enumeración de una sección. |
| virtual [VisitShapeEnd](../../aspose.words/documentvisitor/visitshapeend/)(Shape) | Se llama cuando finaliza la enumeración de una forma. |
| virtual [VisitShapeStart](../../aspose.words/documentvisitor/visitshapestart/)(Shape) | Llamado cuando ha comenzado la enumeración de una forma. |
| virtual [VisitSmartTagEnd](../../aspose.words/documentvisitor/visitsmarttagend/)(SmartTag) | Se llama cuando finaliza la enumeración de una etiqueta inteligente. |
| virtual [VisitSmartTagStart](../../aspose.words/documentvisitor/visitsmarttagstart/)(SmartTag) | Llamado cuando ha comenzado la enumeración de una etiqueta inteligente. |
| virtual [VisitSpecialChar](../../aspose.words/documentvisitor/visitspecialchar/)(SpecialChar) | Llamado cuando un[`SpecialChar`](../specialchar/) nodo se encuentra en el documento. |
| virtual [VisitStructuredDocumentTagEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagend/)(StructuredDocumentTag) | Se llama cuando finaliza la enumeración de una etiqueta de documento estructurado. |
| virtual [VisitStructuredDocumentTagRangeEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagrangeend/)(StructuredDocumentTagRangeEnd) |  |
| virtual [VisitStructuredDocumentTagRangeStart](../../aspose.words/documentvisitor/visitstructureddocumenttagrangestart/)(StructuredDocumentTagRangeStart) |  |
| virtual [VisitStructuredDocumentTagStart](../../aspose.words/documentvisitor/visitstructureddocumenttagstart/)(StructuredDocumentTag) | Llamado cuando ha comenzado la enumeración de una etiqueta de documento estructurado. |
| virtual [VisitSubDocument](../../aspose.words/documentvisitor/visitsubdocument/)(SubDocument) | Llamado cuando se encuentra un subdocumento. |
| virtual [VisitTableEnd](../../aspose.words/documentvisitor/visittableend/)(Table) | Se llama cuando finaliza la enumeración de una tabla. |
| virtual [VisitTableStart](../../aspose.words/documentvisitor/visittablestart/)(Table) | Llamado cuando se ha iniciado la enumeración de una tabla. |

### Observaciones

Con **Visitante del documento** puede definir y ejecutar operaciones personalizadas que requieren enumeración en el árbol del documento.

Por ejemplo, Aspose.Words utiliza **Visitante del documento** internamente para ahorrar **Documento** en varios formatos y para otras operaciones como encontrar campos o marcadores sobre un fragmento de un documento.

Usar **Visitante del documento**:

1. Crear una clase derivada de **Visitante del documento**.
2. Anule y proporcione implementaciones para algunos o todos los métodos VisitXXX para realizar algunas operaciones personalizadas.
3. Llamar[`Nodo.Aceptar`](../node/accept/) sobre el **Nodo** that desde el que desea iniciar la enumeración.

**Visitante del documento**proporciona implementaciones predeterminadas para todos los métodos VisitXXX para facilitar la creación de nuevos visitantes de documentos, ya que solo los métodos necesarios para el visitante particular deben anularse. No es necesario anular todos los métodos de visitante.

Para obtener más información, consulte el patrón de diseño Visitante.

### Ejemplos

Muestra cómo usar un visitante de documentos para imprimir la estructura de nodos de un documento.

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // Cuando conseguimos que un nodo compuesto acepte un documento visitante, el visitante visita el nodo de aceptación,
    // y luego atraviesa todos los elementos secundarios del nodo en profundidad.
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
    /// Llamado cuando se encuentra un nodo de documento.
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
    /// Llamado después de que se hayan visitado todos los nodos secundarios de un nodo de documento.
    /// </summary>
    public override VisitorAction VisitDocumentEnd(Document doc)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Document end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo Sección en el documento.
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
    /// Llamado después de que se hayan visitado todos los nodos secundarios de un nodo Sección.
    /// </summary>
    public override VisitorAction VisitSectionEnd(Section section)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Section end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo Cuerpo en el documento.
    /// </summary>
    public override VisitorAction VisitBodyStart(Body body)
    {
        int paragraphCount = body.Paragraphs.Count;
        IndentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado después de que se hayan visitado todos los nodos secundarios de un nodo Cuerpo.
    /// </summary>
    public override VisitorAction VisitBodyEnd(Body body)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Body end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo de párrafo en el documento.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        IndentAndAppendLine("[Paragraph start]");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado después de que se hayan visitado todos los nodos secundarios de un nodo Paragraph.
    /// </summary>
    public override VisitorAction VisitParagraphEnd(Paragraph paragraph)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Paragraph end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo Ejecutar en el documento.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo SubDocument en el documento.
    /// </summary>
    public override VisitorAction VisitSubDocument(SubDocument subDocument)
    {
        IndentAndAppendLine("[SubDocument]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Agregue una línea al StringBuilder y sangre dependiendo de qué tan profundo esté el visitante en el árbol del documento.
    /// </summary>
    /// <parámetro nombre="texto"></parámetro>
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


