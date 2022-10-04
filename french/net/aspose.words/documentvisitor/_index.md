---
title: DocumentVisitor
second_title: Référence de l'API Aspose.Words pour .NET
description: Classe de base pour les visiteurs de documents personnalisés.
type: docs
weight: 460
url: /fr/net/aspose.words/documentvisitor/
---
## DocumentVisitor class

Classe de base pour les visiteurs de documents personnalisés.

```csharp
public abstract class DocumentVisitor
```

## Méthodes

| Nom | La description |
| --- | --- |
| virtual [VisitAbsolutePositionTab](../../aspose.words/documentvisitor/visitabsolutepositiontab/)(AbsolutePositionTab) | Appelé lorsqu'un[`AbsolutePositionTab`](../absolutepositiontab/) nœud est rencontré dans le document. |
| virtual [VisitBodyEnd](../../aspose.words/documentvisitor/visitbodyend/)(Body) | Appelé lorsque l'énumération de l'article de texte principal dans une section est terminée. |
| virtual [VisitBodyStart](../../aspose.words/documentvisitor/visitbodystart/)(Body) | Appelé lorsque l'énumération de l'histoire du texte principal dans une section a commencé. |
| virtual [VisitBookmarkEnd](../../aspose.words/documentvisitor/visitbookmarkend/)(BookmarkEnd) | Appelé lorsqu'une fin de signet est rencontrée dans le document. |
| virtual [VisitBookmarkStart](../../aspose.words/documentvisitor/visitbookmarkstart/)(BookmarkStart) | Appelé lorsqu'un début de signet est rencontré dans le document. |
| virtual [VisitBuildingBlockEnd](../../aspose.words/documentvisitor/visitbuildingblockend/)(BuildingBlock) | Appelé lorsque l'énumération d'un bloc de construction est terminée. |
| virtual [VisitBuildingBlockStart](../../aspose.words/documentvisitor/visitbuildingblockstart/)(BuildingBlock) | Appelé lorsque l'énumération d'un bloc de construction a commencé. |
| virtual [VisitCellEnd](../../aspose.words/documentvisitor/visitcellend/)(Cell) | Appelé lorsque l'énumération d'une cellule du tableau est terminée. |
| virtual [VisitCellStart](../../aspose.words/documentvisitor/visitcellstart/)(Cell) | Appelé lorsque l'énumération d'une cellule du tableau a commencé. |
| virtual [VisitCommentEnd](../../aspose.words/documentvisitor/visitcommentend/)(Comment) | Appelé lorsque l'énumération d'un texte de commentaire est terminée. |
| virtual [VisitCommentRangeEnd](../../aspose.words/documentvisitor/visitcommentrangeend/)(CommentRangeEnd) | Appelé lorsque la fin d'une plage de texte commentée est rencontrée. |
| virtual [VisitCommentRangeStart](../../aspose.words/documentvisitor/visitcommentrangestart/)(CommentRangeStart) | Appelé lorsque le début d'une plage de texte commentée est rencontré. |
| virtual [VisitCommentStart](../../aspose.words/documentvisitor/visitcommentstart/)(Comment) | Appelé lorsque l'énumération d'un texte de commentaire a commencé. |
| virtual [VisitDocumentEnd](../../aspose.words/documentvisitor/visitdocumentend/)(Document) | Appelé lorsque l'énumération du document est terminée. |
| virtual [VisitDocumentStart](../../aspose.words/documentvisitor/visitdocumentstart/)(Document) | Appelé lorsque l'énumération du document a commencé. |
| virtual [VisitEditableRangeEnd](../../aspose.words/documentvisitor/visiteditablerangeend/)(EditableRangeEnd) | Appelé lorsqu'une fin de plage modifiable est rencontrée dans le document. |
| virtual [VisitEditableRangeStart](../../aspose.words/documentvisitor/visiteditablerangestart/)(EditableRangeStart) | Appelé lorsqu'un début de plage modifiable est rencontré dans le document. |
| virtual [VisitFieldEnd](../../aspose.words/documentvisitor/visitfieldend/)(FieldEnd) | Appelé lorsqu'un champ se termine dans le document. |
| virtual [VisitFieldSeparator](../../aspose.words/documentvisitor/visitfieldseparator/)(FieldSeparator) | Appelé lorsqu'un séparateur de champs est rencontré dans le document. |
| virtual [VisitFieldStart](../../aspose.words/documentvisitor/visitfieldstart/)(FieldStart) | Appelé lorsqu'un champ commence dans le document. |
| virtual [VisitFootnoteEnd](../../aspose.words/documentvisitor/visitfootnoteend/)(Footnote) | Appelé lorsque l'énumération d'une note de bas de page ou d'un texte de note de fin est terminée. |
| virtual [VisitFootnoteStart](../../aspose.words/documentvisitor/visitfootnotestart/)(Footnote) | Appelé lorsque l'énumération d'une note de bas de page ou d'un texte de note de fin a commencé. |
| virtual [VisitFormField](../../aspose.words/documentvisitor/visitformfield/)(FormField) | Appelé lorsqu'un champ de formulaire est rencontré dans le document. |
| virtual [VisitGlossaryDocumentEnd](../../aspose.words/documentvisitor/visitglossarydocumentend/)(GlossaryDocument) | Appelé lorsque l'énumération d'un document de glossaire est terminée. |
| virtual [VisitGlossaryDocumentStart](../../aspose.words/documentvisitor/visitglossarydocumentstart/)(GlossaryDocument) | Appelé lorsque l'énumération d'un document de glossaire a commencé. |
| virtual [VisitGroupShapeEnd](../../aspose.words/documentvisitor/visitgroupshapeend/)(GroupShape) | Appelé lorsque l'énumération d'une forme de groupe est terminée. |
| virtual [VisitGroupShapeStart](../../aspose.words/documentvisitor/visitgroupshapestart/)(GroupShape) | Appelé lorsque l'énumération d'une forme de groupe a commencé. |
| virtual [VisitHeaderFooterEnd](../../aspose.words/documentvisitor/visitheaderfooterend/)(HeaderFooter) | Appelé lorsque l'énumération d'un en-tête ou d'un pied de page dans une section est terminée. |
| virtual [VisitHeaderFooterStart](../../aspose.words/documentvisitor/visitheaderfooterstart/)(HeaderFooter) | Appelé lorsque l'énumération d'un en-tête ou d'un pied de page dans une section a commencé. |
| virtual [VisitOfficeMathEnd](../../aspose.words/documentvisitor/visitofficemathend/)(OfficeMath) | Appelé lorsque l'énumération d'un objet Office Math est terminée. |
| virtual [VisitOfficeMathStart](../../aspose.words/documentvisitor/visitofficemathstart/)(OfficeMath) | Appelé lorsque l'énumération d'un objet Office Math a commencé. |
| virtual [VisitParagraphEnd](../../aspose.words/documentvisitor/visitparagraphend/)(Paragraph) | Appelé lorsque l'énumération d'un paragraphe est terminée. |
| virtual [VisitParagraphStart](../../aspose.words/documentvisitor/visitparagraphstart/)(Paragraph) | Appelé lorsque l'énumération d'un paragraphe a commencé. |
| virtual [VisitRowEnd](../../aspose.words/documentvisitor/visitrowend/)(Row) | Appelé lorsque l'énumération d'une ligne de table est terminée. |
| virtual [VisitRowStart](../../aspose.words/documentvisitor/visitrowstart/)(Row) | Appelé lorsque l'énumération d'une ligne de table a commencé. |
| virtual [VisitRun](../../aspose.words/documentvisitor/visitrun/)(Run) | Appelé lorsqu'une suite de texte dans le est rencontrée. |
| virtual [VisitSectionEnd](../../aspose.words/documentvisitor/visitsectionend/)(Section) | Appelé lorsque l'énumération d'une section est terminée. |
| virtual [VisitSectionStart](../../aspose.words/documentvisitor/visitsectionstart/)(Section) | Appelé lorsque l'énumération d'une section a commencé. |
| virtual [VisitShapeEnd](../../aspose.words/documentvisitor/visitshapeend/)(Shape) | Appelé lorsque l'énumération d'une forme est terminée. |
| virtual [VisitShapeStart](../../aspose.words/documentvisitor/visitshapestart/)(Shape) | Appelé lorsque l'énumération d'une forme a commencé. |
| virtual [VisitSmartTagEnd](../../aspose.words/documentvisitor/visitsmarttagend/)(SmartTag) | Appelé lorsque l'énumération d'une balise active est terminée. |
| virtual [VisitSmartTagStart](../../aspose.words/documentvisitor/visitsmarttagstart/)(SmartTag) | Appelé lorsque l'énumération d'une balise active a commencé. |
| virtual [VisitSpecialChar](../../aspose.words/documentvisitor/visitspecialchar/)(SpecialChar) | Appelé lorsqu'un[`SpecialChar`](../specialchar/) nœud est rencontré dans le document. |
| virtual [VisitStructuredDocumentTagEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagend/)(StructuredDocumentTag) | Appelé lorsque l'énumération d'une balise de document structuré est terminée. |
| virtual [VisitStructuredDocumentTagRangeEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagrangeend/)(StructuredDocumentTagRangeEnd) |  |
| virtual [VisitStructuredDocumentTagRangeStart](../../aspose.words/documentvisitor/visitstructureddocumenttagrangestart/)(StructuredDocumentTagRangeStart) |  |
| virtual [VisitStructuredDocumentTagStart](../../aspose.words/documentvisitor/visitstructureddocumenttagstart/)(StructuredDocumentTag) | Appelé lorsque l'énumération d'une balise de document structuré a commencé. |
| virtual [VisitSubDocument](../../aspose.words/documentvisitor/visitsubdocument/)(SubDocument) | Appelé lorsqu'un sous-document est rencontré. |
| virtual [VisitTableEnd](../../aspose.words/documentvisitor/visittableend/)(Table) | Appelé lorsque l'énumération d'une table est terminée. |
| virtual [VisitTableStart](../../aspose.words/documentvisitor/visittablestart/)(Table) | Appelé lorsque l'énumération d'une table a commencé. |

### Remarques

Avec **DocumentVisitor** vous pouvez définir et exécuter des opérations personnalisées qui nécessitent une énumération sur l'arborescence du document.

Par exemple, Aspose.Words utilise **DocumentVisitor** en interne pour économiser **Document** dans divers formats et pour d'autres opérations telles que la recherche de champs ou de signets sur un fragment d'un document.

Utiliser **DocumentVisitor**:

1. Créer une classe dérivée de **DocumentVisitor**.
2. Remplacez et fournissez des implémentations pour certaines ou toutes les méthodes VisitXXX afin d'effectuer certaines opérations personnalisées.
3. Appel[`Node.Accept`](../node/accept/) sur le **Nœud** that à partir duquel vous voulez commencer l'énumération.

**DocumentVisitor**fournit des implémentations par défaut pour toutes les méthodes VisitXXX afin de faciliter la création de nouveaux visiteurs de document car seules les méthodes requises pour le visiteur particulier doivent être remplacées. Il n'est pas nécessaire de remplacer toutes les méthodes de visiteur.

Pour plus d'informations, consultez le modèle de conception Visiteur.

### Exemples

Montre comment utiliser un visiteur de document pour imprimer la structure de nœud d'un document.

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // Lorsque nous obtenons un nœud composite pour accepter un visiteur de document, le visiteur visite le nœud acceptant,
    // puis parcourt tous les enfants du nœud en profondeur d'abord.
    // Le visiteur peut lire et modifier chaque nœud visité.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Parcourt l'arborescence des nœuds enfants d'un nœud.
/// Crée une carte de cet arbre sous la forme d'une chaîne.
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
    /// Appelé lorsqu'un nœud Document est rencontré.
    /// </summary>
    public override VisitorAction VisitDocumentStart(Document doc)
    {
        int childNodeCount = doc.GetChildNodes(NodeType.Any, true).Count;

        IndentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
        mDocTraversalDepth++;

        // Autoriser le visiteur à continuer à visiter d'autres nœuds.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé après que tous les nœuds enfants d'un nœud Document ont été visités.
    /// </summary>
    public override VisitorAction VisitDocumentEnd(Document doc)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Document end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud Section est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitSectionStart(Section section)
    {
        // Récupère l'index de notre section dans le document.
        NodeCollection docSections = section.Document.GetChildNodes(NodeType.Section, false);
        int sectionIndex = docSections.IndexOf(section);

        IndentAndAppendLine("[Section start] Section index: " + sectionIndex);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé après que tous les nœuds enfants d'un nœud Section ont été visités.
    /// </summary>
    public override VisitorAction VisitSectionEnd(Section section)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Section end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud Body est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitBodyStart(Body body)
    {
        int paragraphCount = body.Paragraphs.Count;
        IndentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé après que tous les nœuds enfants d'un nœud Body ont été visités.
    /// </summary>
    public override VisitorAction VisitBodyEnd(Body body)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Body end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud Paragraphe est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        IndentAndAppendLine("[Paragraph start]");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé après que tous les nœuds enfants d'un nœud Paragraphe ont été visités.
    /// </summary>
    public override VisitorAction VisitParagraphEnd(Paragraph paragraph)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Paragraph end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un noeud Run est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsqu'un nœud SubDocument est rencontré dans le document.
    /// </summary>
    public override VisitorAction VisitSubDocument(SubDocument subDocument)
    {
        IndentAndAppendLine("[SubDocument]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Ajoutez une ligne au StringBuilder et indentez-la en fonction de la profondeur du visiteur dans l'arborescence du document.
    /// </summary>
    /// <nom du paramètre="texte"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mAcceptingNodeChildTree.Append("|  ");

        mAcceptingNodeChildTree.AppendLine(text);
    }

    private int mDocTraversalDepth;
    private readonly StringBuilder mAcceptingNodeChildTree;
}
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
