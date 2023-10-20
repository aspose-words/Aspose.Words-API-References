---
title: DocumentVisitor Class
linktitle: DocumentVisitor
articleTitle: DocumentVisitor
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.DocumentVisitor 班级. 自定义文档访问者的基类 在 C#.
type: docs
weight: 470
url: /zh/net/aspose.words/documentvisitor/
---
## DocumentVisitor class

自定义文档访问者的基类。

要了解更多信息，请访问[Aspose.Words 文档对象模型 (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/)文档文章。

```csharp
public abstract class DocumentVisitor
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| virtual [VisitAbsolutePositionTab](../../aspose.words/documentvisitor/visitabsolutepositiontab/)(*[AbsolutePositionTab](../absolutepositiontab/)*) | 当 a 时调用[`AbsolutePositionTab`](../absolutepositiontab/)文档中遇到节点。 |
| virtual [VisitBodyEnd](../../aspose.words/documentvisitor/visitbodyend/)(*[Body](../body/)*) | 当章节中主要文本故事的枚举结束时调用。 |
| virtual [VisitBodyStart](../../aspose.words/documentvisitor/visitbodystart/)(*[Body](../body/)*) | 当开始枚举章节中的主要文本故事时调用。 |
| virtual [VisitBookmarkEnd](../../aspose.words/documentvisitor/visitbookmarkend/)(*[BookmarkEnd](../bookmarkend/)*) | 在文档中遇到书签末尾时调用。 |
| virtual [VisitBookmarkStart](../../aspose.words/documentvisitor/visitbookmarkstart/)(*[BookmarkStart](../bookmarkstart/)*) | 在文档中遇到书签的开头时调用。 |
| virtual [VisitBuildingBlockEnd](../../aspose.words/documentvisitor/visitbuildingblockend/)(*[BuildingBlock](../../aspose.words.buildingblocks/buildingblock/)*) | 当构建块枚举结束时调用。 |
| virtual [VisitBuildingBlockStart](../../aspose.words/documentvisitor/visitbuildingblockstart/)(*[BuildingBlock](../../aspose.words.buildingblocks/buildingblock/)*) | 在开始枚举构建块时调用。 |
| virtual [VisitCellEnd](../../aspose.words/documentvisitor/visitcellend/)(*[Cell](../../aspose.words.tables/cell/)*) | 当表格单元格枚举结束时调用。 |
| virtual [VisitCellStart](../../aspose.words/documentvisitor/visitcellstart/)(*[Cell](../../aspose.words.tables/cell/)*) | 在开始枚举表格单元格时调用。 |
| virtual [VisitCommentEnd](../../aspose.words/documentvisitor/visitcommentend/)(*[Comment](../comment/)*) | 当注释文本枚举结束时调用。 |
| virtual [VisitCommentRangeEnd](../../aspose.words/documentvisitor/visitcommentrangeend/)(*[CommentRangeEnd](../commentrangeend/)*) | 当遇到注释文本范围的末尾时调用。 |
| virtual [VisitCommentRangeStart](../../aspose.words/documentvisitor/visitcommentrangestart/)(*[CommentRangeStart](../commentrangestart/)*) | 当遇到注释文本范围的开头时调用。 |
| virtual [VisitCommentStart](../../aspose.words/documentvisitor/visitcommentstart/)(*[Comment](../comment/)*) | 开始枚举注释文本时调用。 |
| virtual [VisitDocumentEnd](../../aspose.words/documentvisitor/visitdocumentend/)(*[Document](../document/)*) | 文档枚举完成后调用。 |
| virtual [VisitDocumentStart](../../aspose.words/documentvisitor/visitdocumentstart/)(*[Document](../document/)*) | 在开始枚举文档时调用。 |
| virtual [VisitEditableRangeEnd](../../aspose.words/documentvisitor/visiteditablerangeend/)(*[EditableRangeEnd](../editablerangeend/)*) | 当文档中遇到可编辑范围的末尾时调用。 |
| virtual [VisitEditableRangeStart](../../aspose.words/documentvisitor/visiteditablerangestart/)(*[EditableRangeStart](../editablerangestart/)*) | 在文档中遇到可编辑范围的开头时调用。 |
| virtual [VisitFieldEnd](../../aspose.words/documentvisitor/visitfieldend/)(*[FieldEnd](../../aspose.words.fields/fieldend/)*) | 当文档中的字段结束时调用。 |
| virtual [VisitFieldSeparator](../../aspose.words/documentvisitor/visitfieldseparator/)(*[FieldSeparator](../../aspose.words.fields/fieldseparator/)*) | 在文档中遇到字段分隔符时调用。 |
| virtual [VisitFieldStart](../../aspose.words/documentvisitor/visitfieldstart/)(*[FieldStart](../../aspose.words.fields/fieldstart/)*) | 当字段在文档中开始时调用。 |
| virtual [VisitFootnoteEnd](../../aspose.words/documentvisitor/visitfootnoteend/)(*[Footnote](../../aspose.words.notes/footnote/)*) | 当脚注或尾注文本的枚举结束时调用。 |
| virtual [VisitFootnoteStart](../../aspose.words/documentvisitor/visitfootnotestart/)(*[Footnote](../../aspose.words.notes/footnote/)*) | 开始枚举脚注或尾注文本时调用。 |
| virtual [VisitFormField](../../aspose.words/documentvisitor/visitformfield/)(*[FormField](../../aspose.words.fields/formfield/)*) | 在文档中遇到表单字段时调用。 |
| virtual [VisitGlossaryDocumentEnd](../../aspose.words/documentvisitor/visitglossarydocumentend/)(*[GlossaryDocument](../../aspose.words.buildingblocks/glossarydocument/)*) | 术语表文档枚举结束时调用。 |
| virtual [VisitGlossaryDocumentStart](../../aspose.words/documentvisitor/visitglossarydocumentstart/)(*[GlossaryDocument](../../aspose.words.buildingblocks/glossarydocument/)*) | 在词汇表文档枚举开始时调用。 |
| virtual [VisitGroupShapeEnd](../../aspose.words/documentvisitor/visitgroupshapeend/)(*[GroupShape](../../aspose.words.drawing/groupshape/)*) | 当组形状枚举结束时调用。 |
| virtual [VisitGroupShapeStart](../../aspose.words/documentvisitor/visitgroupshapestart/)(*[GroupShape](../../aspose.words.drawing/groupshape/)*) | 在开始枚举组形状时调用。 |
| virtual [VisitHeaderFooterEnd](../../aspose.words/documentvisitor/visitheaderfooterend/)(*[HeaderFooter](../headerfooter/)*) | 当节中页眉或页脚的枚举结束时调用。 |
| virtual [VisitHeaderFooterStart](../../aspose.words/documentvisitor/visitheaderfooterstart/)(*[HeaderFooter](../headerfooter/)*) | 当开始枚举节中的页眉或页脚时调用。 |
| virtual [VisitOfficeMathEnd](../../aspose.words/documentvisitor/visitofficemathend/)(*[OfficeMath](../../aspose.words.math/officemath/)*) | 当 Office Math 对象的枚举结束时调用。 |
| virtual [VisitOfficeMathStart](../../aspose.words/documentvisitor/visitofficemathstart/)(*[OfficeMath](../../aspose.words.math/officemath/)*) | 在开始枚举 Office Math 对象时调用。 |
| virtual [VisitParagraphEnd](../../aspose.words/documentvisitor/visitparagraphend/)(*[Paragraph](../paragraph/)*) | 段落枚举结束时调用。 |
| virtual [VisitParagraphStart](../../aspose.words/documentvisitor/visitparagraphstart/)(*[Paragraph](../paragraph/)*) | 开始枚举段落时调用。 |
| virtual [VisitRowEnd](../../aspose.words/documentvisitor/visitrowend/)(*[Row](../../aspose.words.tables/row/)*) | 当表行枚举结束时调用。 |
| virtual [VisitRowStart](../../aspose.words/documentvisitor/visitrowstart/)(*[Row](../../aspose.words.tables/row/)*) | 在开始枚举表行时调用。 |
| virtual [VisitRun](../../aspose.words/documentvisitor/visitrun/)(*[Run](../run/)*) | 当遇到文本运行时调用。 |
| virtual [VisitSectionEnd](../../aspose.words/documentvisitor/visitsectionend/)(*[Section](../section/)*) | 当节的枚举结束时调用。 |
| virtual [VisitSectionStart](../../aspose.words/documentvisitor/visitsectionstart/)(*[Section](../section/)*) | 在开始枚举节时调用。 |
| virtual [VisitShapeEnd](../../aspose.words/documentvisitor/visitshapeend/)(*[Shape](../../aspose.words.drawing/shape/)*) | 当形状枚举结束时调用。 |
| virtual [VisitShapeStart](../../aspose.words/documentvisitor/visitshapestart/)(*[Shape](../../aspose.words.drawing/shape/)*) | 当开始枚举形状时调用。 |
| virtual [VisitSmartTagEnd](../../aspose.words/documentvisitor/visitsmarttagend/)(*[SmartTag](../../aspose.words.markup/smarttag/)*) | 智能标记枚举结束时调用。 |
| virtual [VisitSmartTagStart](../../aspose.words/documentvisitor/visitsmarttagstart/)(*[SmartTag](../../aspose.words.markup/smarttag/)*) | 在开始枚举智能标记时调用。 |
| virtual [VisitSpecialChar](../../aspose.words/documentvisitor/visitspecialchar/)(*[SpecialChar](../specialchar/)*) | 当 a 时调用[`SpecialChar`](../specialchar/)文档中遇到节点。 |
| virtual [VisitStructuredDocumentTagEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagend/)(*[StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/)*) | 当结构化文档标签的枚举结束时调用。 |
| virtual [VisitStructuredDocumentTagRangeEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagrangeend/)(*[StructuredDocumentTagRangeEnd](../../aspose.words.markup/structureddocumenttagrangeend/)*) | 遇到 StructuredDocumentTagRangeEnd 时调用。 |
| virtual [VisitStructuredDocumentTagRangeStart](../../aspose.words/documentvisitor/visitstructureddocumenttagrangestart/)(*[StructuredDocumentTagRangeStart](../../aspose.words.markup/structureddocumenttagrangestart/)*) | 遇到 StructuredDocumentTagRangeStart 时调用。 |
| virtual [VisitStructuredDocumentTagStart](../../aspose.words/documentvisitor/visitstructureddocumenttagstart/)(*[StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/)*) | 开始枚举结构化文档标记时调用。 |
| virtual [VisitSubDocument](../../aspose.words/documentvisitor/visitsubdocument/)(*[SubDocument](../subdocument/)*) | 遇到子文档时调用。 |
| virtual [VisitTableEnd](../../aspose.words/documentvisitor/visittableend/)(*[Table](../../aspose.words.tables/table/)*) | 表枚举结束时调用。 |
| virtual [VisitTableStart](../../aspose.words/documentvisitor/visittablestart/)(*[Table](../../aspose.words.tables/table/)*) | 在开始枚举表时调用。 |

## 评论

和`DocumentVisitor`您可以定义并执行需要枚举文档树的自定义操作 。

例如，Aspose.Words 使用`DocumentVisitor`内部保存[`Document`](../document/) 各种格式以及其他操作，例如在 文档片段上查找字段或书签。

使用`DocumentVisitor`:

1. 创建一个派生类`DocumentVisitor`。
2. 重写并提供部分或全部 VisitXXX 方法 的实现，以执行一些自定义操作。
3. 称呼[`节点接受`](../node/accept/)于[`Node`](../node/)that 您想要从中开始枚举。

`DocumentVisitor`为所有 VisitXXX 方法 提供默认实现，以便更轻松地创建新文档访问者，因为只需要重写特定 访问者所需的方法。没有必要重写所有访问者方法。

有关详细信息，请参阅访客设计模式。

## 例子

演示如何使用文档访问者打印文档的节点结构。

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // 当我们得到一个复合节点来接受文档访问者时，访问者访问接受节点，
    // 然后以深度优先的方式遍历该节点的所有子节点。
    // 访问者可以读取和修改每个访问过的节点。
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// 遍历节点的子节点树。
/// 以字符串的形式创建该树的映射。
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
    /// 在访问 Document 节点的所有子节点后调用。
    /// </summary>
    public override VisitorAction VisitDocumentEnd(Document doc)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Document end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到Section 节点时调用。
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
    /// 在访问了Section节点的所有子节点后调用。
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
    /// 在访问了 Body 节点的所有子节点后调用。
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
    /// 在访问 Paragraph 节点的所有子节点后调用。
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
    /// 在文档中遇到 SubDocument 节点时调用。
    /// </summary>
    public override VisitorAction VisitSubDocument(SubDocument subDocument)
    {
        IndentAndAppendLine("[SubDocument]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 将一行追加到 StringBuilder 并根据访问者在文档树中的深度对其进行缩进。
    /// </summary>
    /// <param name="text"></param>;
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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
