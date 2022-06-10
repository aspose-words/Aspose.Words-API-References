---
title: DocumentVisitor
second_title: Aspose.Words for .NET API 参考
description: 自定义文档访问者的基类
type: docs
weight: 460
url: /zh/net/aspose.words/documentvisitor/
---
## DocumentVisitor class

自定义文档访问者的基类。

```csharp
public abstract class DocumentVisitor
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| virtual [VisitAbsolutePositionTab](../../aspose.words/documentvisitor/visitabsolutepositiontab)(AbsolutePositionTab) | 在文档中遇到[`AbsolutePositionTab`](../absolutepositiontab)节点时调用。 |
| virtual [VisitBodyEnd](../../aspose.words/documentvisitor/visitbodyend)(Body) | 当一节中的正文故事的枚举结束时调用。 |
| virtual [VisitBodyStart](../../aspose.words/documentvisitor/visitbodystart)(Body) | 当一节中的正文故事的枚举开始时调用。 |
| virtual [VisitBookmarkEnd](../../aspose.words/documentvisitor/visitbookmarkend)(BookmarkEnd) | 在文档中遇到书签结尾时调用。 |
| virtual [VisitBookmarkStart](../../aspose.words/documentvisitor/visitbookmarkstart)(BookmarkStart) | 在文档中遇到书签开始时调用。 |
| virtual [VisitBuildingBlockEnd](../../aspose.words/documentvisitor/visitbuildingblockend)(BuildingBlock) | 在构建块的枚举结束时调用。 |
| virtual [VisitBuildingBlockStart](../../aspose.words/documentvisitor/visitbuildingblockstart)(BuildingBlock) | 在开始枚举构建块时调用。 |
| virtual [VisitCellEnd](../../aspose.words/documentvisitor/visitcellend)(Cell) | 在表格单元格的枚举结束时调用。 |
| virtual [VisitCellStart](../../aspose.words/documentvisitor/visitcellstart)(Cell) | 在开始枚举表格单元格时调用。 |
| virtual [VisitCommentEnd](../../aspose.words/documentvisitor/visitcommentend)(Comment) | 注释文本枚举结束时调用。 |
| virtual [VisitCommentRangeEnd](../../aspose.words/documentvisitor/visitcommentrangeend)(CommentRangeEnd) | 当遇到注释文本范围的结尾时调用。 |
| virtual [VisitCommentRangeStart](../../aspose.words/documentvisitor/visitcommentrangestart)(CommentRangeStart) | 在遇到注释文本范围的开头时调用。 |
| virtual [VisitCommentStart](../../aspose.words/documentvisitor/visitcommentstart)(Comment) | 注释文本枚举开始时调用。 |
| virtual [VisitDocumentEnd](../../aspose.words/documentvisitor/visitdocumentend)(Document) | 当文档的枚举完成时调用。 |
| virtual [VisitDocumentStart](../../aspose.words/documentvisitor/visitdocumentstart)(Document) | 在文档枚举开始时调用。 |
| virtual [VisitEditableRangeEnd](../../aspose.words/documentvisitor/visiteditablerangeend)(EditableRangeEnd) | 在文档中遇到可编辑范围的结尾时调用。 |
| virtual [VisitEditableRangeStart](../../aspose.words/documentvisitor/visiteditablerangestart)(EditableRangeStart) | 在文档中遇到可编辑范围的开始时调用。 |
| virtual [VisitFieldEnd](../../aspose.words/documentvisitor/visitfieldend)(FieldEnd) | 当字段在文档中结束时调用。 |
| virtual [VisitFieldSeparator](../../aspose.words/documentvisitor/visitfieldseparator)(FieldSeparator) | 在文档中遇到字段分隔符时调用。 |
| virtual [VisitFieldStart](../../aspose.words/documentvisitor/visitfieldstart)(FieldStart) | 当文档中的字段开始时调用。 |
| virtual [VisitFootnoteEnd](../../aspose.words/documentvisitor/visitfootnoteend)(Footnote) | 当脚注或尾注文本的枚举结束时调用。 |
| virtual [VisitFootnoteStart](../../aspose.words/documentvisitor/visitfootnotestart)(Footnote) | 在脚注或尾注文本的枚举开始时调用。 |
| virtual [VisitFormField](../../aspose.words/documentvisitor/visitformfield)(FormField) | 在文档中遇到表单字段时调用。 |
| virtual [VisitGlossaryDocumentEnd](../../aspose.words/documentvisitor/visitglossarydocumentend)(GlossaryDocument) | 在词汇表文档的枚举结束时调用。 |
| virtual [VisitGlossaryDocumentStart](../../aspose.words/documentvisitor/visitglossarydocumentstart)(GlossaryDocument) | 在开始枚举词汇表文档时调用。 |
| virtual [VisitGroupShapeEnd](../../aspose.words/documentvisitor/visitgroupshapeend)(GroupShape) | 当组形状的枚举结束时调用。 |
| virtual [VisitGroupShapeStart](../../aspose.words/documentvisitor/visitgroupshapestart)(GroupShape) | 在开始枚举组形状时调用。 |
| virtual [VisitHeaderFooterEnd](../../aspose.words/documentvisitor/visitheaderfooterend)(HeaderFooter) | 当节中的页眉或页脚枚举结束时调用。 |
| virtual [VisitHeaderFooterStart](../../aspose.words/documentvisitor/visitheaderfooterstart)(HeaderFooter) | 在开始枚举节中的页眉或页脚时调用。 |
| virtual [VisitOfficeMathEnd](../../aspose.words/documentvisitor/visitofficemathend)(OfficeMath) | 在 Office Math 对象的枚举结束时调用。 |
| virtual [VisitOfficeMathStart](../../aspose.words/documentvisitor/visitofficemathstart)(OfficeMath) | 在 Office Math 对象的枚举开始时调用。 |
| virtual [VisitParagraphEnd](../../aspose.words/documentvisitor/visitparagraphend)(Paragraph) | 段落枚举结束时调用。 |
| virtual [VisitParagraphStart](../../aspose.words/documentvisitor/visitparagraphstart)(Paragraph) | 段落枚举开始时调用。 |
| virtual [VisitRowEnd](../../aspose.words/documentvisitor/visitrowend)(Row) | 表行枚举结束时调用。 |
| virtual [VisitRowStart](../../aspose.words/documentvisitor/visitrowstart)(Row) | 在开始枚举表行时调用。 |
| virtual [VisitRun](../../aspose.words/documentvisitor/visitrun)(Run) | 在遇到文本运行时调用。 |
| virtual [VisitSectionEnd](../../aspose.words/documentvisitor/visitsectionend)(Section) | 当一个节的枚举结束时调用。 |
| virtual [VisitSectionStart](../../aspose.words/documentvisitor/visitsectionstart)(Section) | 当节的枚举开始时调用。 |
| virtual [VisitShapeEnd](../../aspose.words/documentvisitor/visitshapeend)(Shape) | 形状枚举结束时调用。 |
| virtual [VisitShapeStart](../../aspose.words/documentvisitor/visitshapestart)(Shape) | 在形状枚举开始时调用。 |
| virtual [VisitSmartTagEnd](../../aspose.words/documentvisitor/visitsmarttagend)(SmartTag) | 当智能标签的枚举结束时调用。 |
| virtual [VisitSmartTagStart](../../aspose.words/documentvisitor/visitsmarttagstart)(SmartTag) | 当智能标签的枚举开始时调用。 |
| virtual [VisitSpecialChar](../../aspose.words/documentvisitor/visitspecialchar)(SpecialChar) | 在文档中遇到[`SpecialChar`](../specialchar)节点时调用。 |
| virtual [VisitStructuredDocumentTagEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagend)(StructuredDocumentTag) | 当结构化文档标签的枚举结束时调用。 |
| virtual [VisitStructuredDocumentTagRangeEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagrangeend)(StructuredDocumentTagRangeEnd) |  |
| virtual [VisitStructuredDocumentTagRangeStart](../../aspose.words/documentvisitor/visitstructureddocumenttagrangestart)(StructuredDocumentTagRangeStart) |  |
| virtual [VisitStructuredDocumentTagStart](../../aspose.words/documentvisitor/visitstructureddocumenttagstart)(StructuredDocumentTag) | 在结构化文档标签的枚举开始时调用。 |
| virtual [VisitSubDocument](../../aspose.words/documentvisitor/visitsubdocument)(SubDocument) | 在遇到子文档时调用。 |
| virtual [VisitTableEnd](../../aspose.words/documentvisitor/visittableend)(Table) | 在表的枚举结束时调用。 |
| virtual [VisitTableStart](../../aspose.words/documentvisitor/visittablestart)(Table) | 在表的枚举开始时调用。 |

### 评论

与 **DocumentVisitor** 你可以定义和执行需要对文档树进行枚举的自定义操作 。

例如，Aspose.Words 在内部使用 **DocumentVisitor** 用于保存 **Document** 以各种格式和其他操作，例如在 文档片段上查找字段或书签。

使用 **DocumentVisitor** :

1. 创建一个派生自 **DocumentVisitor** 的类。
2. 覆盖并提供部分或全部 VisitXXX 方法的实现 以执行一些自定义操作。
3. 调用[`Node.Accept`](../node/accept):: 在 **节点** 上 您要从其开始枚举。

**DocumentVisitor** 为所有 VisitXXX 方法提供默认实现 使创建新文档访问者更容易，因为只有特定 访问者所需的方法需要被覆盖。没有必要覆盖所有的访问者方法。

有关更多信息，请参阅访问者设计模式。

### 例子

显示如何使用文档访问者打印文档的节点结构。

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

     // 当我们得到一个复合节点接受一个文档访问者时，访问者访问接受节点，
     // 然后以深度优先的方式遍历所有节点的孩子。
     // 访问者可以读取和修改每个访问过的节点。
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// 遍历一个节点的子节点树。
 /// 以字符串的形式创建这棵树的映射。
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
     /// 遇到 Document 节点时调用。
    /// </summary>
    public override VisitorAction VisitDocumentStart(Document doc)
    {
        int childNodeCount = doc.GetChildNodes(NodeType.Any, true).Count;

        IndentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
        mDocTraversalDepth++;

         // 允许访问者继续访问其他节点。
        return VisitorAction.Continue;
    }

    /// <summary>
     /// 在一个 Document 节点的所有子节点都被访问后调用。
    /// </summary>
    public override VisitorAction VisitDocumentEnd(Document doc)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Document end]");

        return VisitorAction.Continue;
    }

    /// <summary>
     /// 在文档中遇到Section节点时调用。
    /// </summary>
    public override VisitorAction VisitSectionStart(Section section)
    {
         // 获取文档中我们部分的索引。
        NodeCollection docSections = section.Document.GetChildNodes(NodeType.Section, false);
        int sectionIndex = docSections.IndexOf(section);

        IndentAndAppendLine("[Section start] Section index: " + sectionIndex);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
     /// 在一个Section节点的所有子节点都被访问后调用。
    /// </summary>
    public override VisitorAction VisitSectionEnd(Section section)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Section end]");

        return VisitorAction.Continue;
    }

    /// <summary>
     /// 在文档中遇到 Body 节点时调用。
    /// </summary>
    public override VisitorAction VisitBodyStart(Body body)
    {
        int paragraphCount = body.Paragraphs.Count;
        IndentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
     /// 在访问完 Body 节点的所有子节点后调用。
    /// </summary>
    public override VisitorAction VisitBodyEnd(Body body)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Body end]");

        return VisitorAction.Continue;
    }

    /// <summary>
     /// 在文档中遇到段落节点时调用。
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        IndentAndAppendLine("[Paragraph start]");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
     /// 在访问完一个段落节点的所有子节点后调用。
    /// </summary>
    public override VisitorAction VisitParagraphEnd(Paragraph paragraph)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Paragraph end]");

        return VisitorAction.Continue;
    }

    /// <summary>
     /// 在文档中遇到 Run 节点时调用。
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到子文档节点时调用。
    /// </summary>
    public override VisitorAction VisitSubDocument(SubDocument subDocument)
    {
        IndentAndAppendLine("[SubDocument]");

        return VisitorAction.Continue;
    }

    /// <summary>
     /// 将一行添加到 StringBuilder 并根据访问者在文档树中的深度缩进。
    /// </summary>
     /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mAcceptingNodeChildTree.Append("|  ");

        mAcceptingNodeChildTree.AppendLine(text);
    }

    private int mDocTraversalDepth;
    private readonly StringBuilder mAcceptingNodeChildTree;
}
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
