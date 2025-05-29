---
title: DocumentVisitor Class
linktitle: DocumentVisitor
articleTitle: DocumentVisitor
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.DocumentVisitor 类，这是创建自定义文档访问者以增强文档处理和操作的基础。
type: docs
weight: 690
url: /zh/net/aspose.words/documentvisitor/
---
## DocumentVisitor class

自定义文档访问者的基类。

要了解更多信息，请访问[Aspose.Words 文档对象模型（DOM）](https://docs.aspose.com/words/net/aspose-words-document-object-model/)文档文章。

```csharp
public abstract class DocumentVisitor
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| virtual [VisitAbsolutePositionTab](../../aspose.words/documentvisitor/visitabsolutepositiontab/)(*[AbsolutePositionTab](../absolutepositiontab/)*) | 当[`AbsolutePositionTab`](../absolutepositiontab/)文档中遇到节点。 |
| virtual [VisitBodyEnd](../../aspose.words/documentvisitor/visitbodyend/)(*[Body](../body/)*) | 当某一部分的主要文本故事枚举结束时调用。 |
| virtual [VisitBodyStart](../../aspose.words/documentvisitor/visitbodystart/)(*[Body](../body/)*) | 当开始枚举某一部分的主要文本故事时调用。 |
| virtual [VisitBookmarkEnd](../../aspose.words/documentvisitor/visitbookmarkend/)(*[BookmarkEnd](../bookmarkend/)*) | 当文档中遇到书签末尾时调用。 |
| virtual [VisitBookmarkStart](../../aspose.words/documentvisitor/visitbookmarkstart/)(*[BookmarkStart](../bookmarkstart/)*) | 当在文档中遇到书签的开头时调用。 |
| virtual [VisitBuildingBlockEnd](../../aspose.words/documentvisitor/visitbuildingblockend/)(*[BuildingBlock](../../aspose.words.buildingblocks/buildingblock/)*) | 当构建块枚举结束时调用。 |
| virtual [VisitBuildingBlockStart](../../aspose.words/documentvisitor/visitbuildingblockstart/)(*[BuildingBlock](../../aspose.words.buildingblocks/buildingblock/)*) | 当构建块的枚举开始时调用。 |
| virtual [VisitCellEnd](../../aspose.words/documentvisitor/visitcellend/)(*[Cell](../../aspose.words.tables/cell/)*) | 当表格单元格的枚举结束时调用。 |
| virtual [VisitCellStart](../../aspose.words/documentvisitor/visitcellstart/)(*[Cell](../../aspose.words.tables/cell/)*) | 当表格单元格的枚举开始时调用。 |
| virtual [VisitCommentEnd](../../aspose.words/documentvisitor/visitcommentend/)(*[Comment](../comment/)*) | 当评论文本枚举结束时调用。 |
| virtual [VisitCommentRangeEnd](../../aspose.words/documentvisitor/visitcommentrangeend/)(*[CommentRangeEnd](../commentrangeend/)*) | 当遇到注释文本范围的末尾时调用。 |
| virtual [VisitCommentRangeStart](../../aspose.words/documentvisitor/visitcommentrangestart/)(*[CommentRangeStart](../commentrangestart/)*) | 当遇到注释文本范围的开头时调用。 |
| virtual [VisitCommentStart](../../aspose.words/documentvisitor/visitcommentstart/)(*[Comment](../comment/)*) | 当开始枚举评论文本时调用。 |
| virtual [VisitDocumentEnd](../../aspose.words/documentvisitor/visitdocumentend/)(*[Document](../document/)*) | 文档枚举完成时调用。 |
| virtual [VisitDocumentStart](../../aspose.words/documentvisitor/visitdocumentstart/)(*[Document](../document/)*) | 在文档枚举开始时调用。 |
| virtual [VisitEditableRangeEnd](../../aspose.words/documentvisitor/visiteditablerangeend/)(*[EditableRangeEnd](../editablerangeend/)*) | 当文档中遇到可编辑范围的末尾时调用。 |
| virtual [VisitEditableRangeStart](../../aspose.words/documentvisitor/visiteditablerangestart/)(*[EditableRangeStart](../editablerangestart/)*) | 当在文档中遇到可编辑范围的开始时调用。 |
| virtual [VisitFieldEnd](../../aspose.words/documentvisitor/visitfieldend/)(*[FieldEnd](../../aspose.words.fields/fieldend/)*) | 当文档中的字段结束时调用。 |
| virtual [VisitFieldSeparator](../../aspose.words/documentvisitor/visitfieldseparator/)(*[FieldSeparator](../../aspose.words.fields/fieldseparator/)*) | 当在文档中遇到字段分隔符时调用。 |
| virtual [VisitFieldStart](../../aspose.words/documentvisitor/visitfieldstart/)(*[FieldStart](../../aspose.words.fields/fieldstart/)*) | 当文档中某个字段开始时调用。 |
| virtual [VisitFootnoteEnd](../../aspose.words/documentvisitor/visitfootnoteend/)(*[Footnote](../../aspose.words.notes/footnote/)*) | 在脚注或尾注文本枚举结束时调用。 |
| virtual [VisitFootnoteStart](../../aspose.words/documentvisitor/visitfootnotestart/)(*[Footnote](../../aspose.words.notes/footnote/)*) | 在开始枚举脚注或尾注文本时调用。 |
| virtual [VisitFormField](../../aspose.words/documentvisitor/visitformfield/)(*[FormField](../../aspose.words.fields/formfield/)*) | 当文档中遇到表单字段时调用。 |
| virtual [VisitGlossaryDocumentEnd](../../aspose.words/documentvisitor/visitglossarydocumentend/)(*[GlossaryDocument](../../aspose.words.buildingblocks/glossarydocument/)*) | 当词汇表文档枚举结束时调用。 |
| virtual [VisitGlossaryDocumentStart](../../aspose.words/documentvisitor/visitglossarydocumentstart/)(*[GlossaryDocument](../../aspose.words.buildingblocks/glossarydocument/)*) | 当词汇表文档的枚举开始时调用。 |
| virtual [VisitGroupShapeEnd](../../aspose.words/documentvisitor/visitgroupshapeend/)(*[GroupShape](../../aspose.words.drawing/groupshape/)*) | 当组形状的枚举结束时调用。 |
| virtual [VisitGroupShapeStart](../../aspose.words/documentvisitor/visitgroupshapestart/)(*[GroupShape](../../aspose.words.drawing/groupshape/)*) | 当组形状的枚举开始时调用。 |
| virtual [VisitHeaderFooterEnd](../../aspose.words/documentvisitor/visitheaderfooterend/)(*[HeaderFooter](../headerfooter/)*) | 当某一部分中的页眉或页脚枚举结束时调用。 |
| virtual [VisitHeaderFooterStart](../../aspose.words/documentvisitor/visitheaderfooterstart/)(*[HeaderFooter](../headerfooter/)*) | 在开始枚举某一部分的页眉或页脚时调用。 |
| virtual [VisitOfficeMathEnd](../../aspose.words/documentvisitor/visitofficemathend/)(*[OfficeMath](../../aspose.words.math/officemath/)*) | 当 Office Math 对象的枚举结束时调用。 |
| virtual [VisitOfficeMathStart](../../aspose.words/documentvisitor/visitofficemathstart/)(*[OfficeMath](../../aspose.words.math/officemath/)*) | 当 Office Math 对象的枚举开始时调用。 |
| virtual [VisitParagraphEnd](../../aspose.words/documentvisitor/visitparagraphend/)(*[Paragraph](../paragraph/)*) | 当段落枚举结束时调用。 |
| virtual [VisitParagraphStart](../../aspose.words/documentvisitor/visitparagraphstart/)(*[Paragraph](../paragraph/)*) | 当段落枚举开始时调用。 |
| virtual [VisitRowEnd](../../aspose.words/documentvisitor/visitrowend/)(*[Row](../../aspose.words.tables/row/)*) | 当表行枚举结束时调用。 |
| virtual [VisitRowStart](../../aspose.words/documentvisitor/visitrowstart/)(*[Row](../../aspose.words.tables/row/)*) | 当表行枚举开始时调用。 |
| virtual [VisitRun](../../aspose.words/documentvisitor/visitrun/)(*[Run](../run/)*) | 当遇到一连串文本时调用。 |
| virtual [VisitSectionEnd](../../aspose.words/documentvisitor/visitsectionend/)(*[Section](../section/)*) | 当某个部分的枚举结束时调用。 |
| virtual [VisitSectionStart](../../aspose.words/documentvisitor/visitsectionstart/)(*[Section](../section/)*) | 当某个部分的枚举开始时调用。 |
| virtual [VisitShapeEnd](../../aspose.words/documentvisitor/visitshapeend/)(*[Shape](../../aspose.words.drawing/shape/)*) | 当形状枚举结束时调用。 |
| virtual [VisitShapeStart](../../aspose.words/documentvisitor/visitshapestart/)(*[Shape](../../aspose.words.drawing/shape/)*) | 当形状枚举开始时调用。 |
| virtual [VisitSmartTagEnd](../../aspose.words/documentvisitor/visitsmarttagend/)(*[SmartTag](../../aspose.words.markup/smarttag/)*) | 当智能标签枚举结束时调用。 |
| virtual [VisitSmartTagStart](../../aspose.words/documentvisitor/visitsmarttagstart/)(*[SmartTag](../../aspose.words.markup/smarttag/)*) | 当智能标签枚举开始时调用。 |
| virtual [VisitSpecialChar](../../aspose.words/documentvisitor/visitspecialchar/)(*[SpecialChar](../specialchar/)*) | 当[`SpecialChar`](../specialchar/)文档中遇到节点。 |
| virtual [VisitStructuredDocumentTagEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagend/)(*[StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/)*) | 当结构化文档标签枚举结束时调用。 |
| virtual [VisitStructuredDocumentTagRangeEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagrangeend/)(*[StructuredDocumentTagRangeEnd](../../aspose.words.markup/structureddocumenttagrangeend/)*) | 遇到 StructuredDocumentTagRangeEnd 时调用。 |
| virtual [VisitStructuredDocumentTagRangeStart](../../aspose.words/documentvisitor/visitstructureddocumenttagrangestart/)(*[StructuredDocumentTagRangeStart](../../aspose.words.markup/structureddocumenttagrangestart/)*) | 遇到 StructuredDocumentTagRangeStart 时调用。 |
| virtual [VisitStructuredDocumentTagStart](../../aspose.words/documentvisitor/visitstructureddocumenttagstart/)(*[StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/)*) | 在结构化文档标签枚举开始时调用。 |
| virtual [VisitSubDocument](../../aspose.words/documentvisitor/visitsubdocument/)(*[SubDocument](../subdocument/)*) | 遇到子文档时调用。 |
| virtual [VisitTableEnd](../../aspose.words/documentvisitor/visittableend/)(*[Table](../../aspose.words.tables/table/)*) | 当表的枚举结束时调用。 |
| virtual [VisitTableStart](../../aspose.words/documentvisitor/visittablestart/)(*[Table](../../aspose.words.tables/table/)*) | 当表的枚举开始时调用。 |

## 评论

和`DocumentVisitor`您可以定义并执行需要对文档树进行枚举的自定义操作 。

例如，Aspose.Words 使用`DocumentVisitor`内部保存[`Document`](../document/) 以各种格式和其他操作（如在文档片段上查找字段或书签）。

使用`DocumentVisitor`：

1. 创建派生自`DocumentVisitor`。
2. 覆盖并提供部分或全部 VisitXXX 方法的实现以执行一些自定义操作。
3. 称呼[`节点.接受`](../node/accept/)在[`Node`](../node/)您想要从中开始枚举的 that 。

`DocumentVisitor`为所有 VisitXXX 方法 提供默认实现，以便于创建新的文档访问者，因为只需重写特定 访问者所需的方法即可。无需重写所有访问者方法。

有关详细信息，请参阅访问者设计模式。

## 例子

展示如何使用文档访问器打印文档的节点结构。

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // 当我们得到一个复合节点来接受文档访问者时，访问者会访问接受节点，
    // 然后以深度优先的方式遍历该节点的所有子节点。
    // 访问者可以读取和修改每个访问的节点。
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// 遍历节点的子节点树。
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
    /// 当遇到 Document 节点时调用。
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
    /// 在访问完 Document 节点的所有子节点后调用。
    /// </summary>
    public override VisitorAction VisitDocumentEnd(Document doc)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Document end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 当在文档中遇到 Section 节点时调用。
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
    /// 在访问完 Section 节点的所有子节点后调用。
    /// </summary>
    public override VisitorAction VisitSectionEnd(Section section)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Section end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 当在文档中遇到 Body 节点时调用。
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
    /// 当在文档中遇到段落节点时调用。
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        IndentAndAppendLine("[Paragraph start]");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在访问完 Paragraph 节点的所有子节点后调用。
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
    /// 当在文档中遇到 SubDocument 节点时调用。
    /// </summary>
    public override VisitorAction VisitSubDocument(SubDocument subDocument)
    {
        IndentAndAppendLine("[SubDocument]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 当在文档中遇到 SubDocument 节点时调用。
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
    {
        IndentAndAppendLine("[SdtRangeStart]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 当在文档中遇到 SubDocument 节点时调用。
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
    {
        IndentAndAppendLine("[SdtRangeEnd]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 向 StringBuilder 附加一行并根据访问者在文档树中的深度进行缩进。
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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
