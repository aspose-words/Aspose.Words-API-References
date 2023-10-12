---
title: Class DocumentVisitor
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.DocumentVisitor сорт. Базовый класс для посетителей пользовательских документов.
type: docs
weight: 470
url: /ru/net/aspose.words/documentvisitor/
---
## DocumentVisitor class

Базовый класс для посетителей пользовательских документов.

Чтобы узнать больше, посетите[Объектная модель документа Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) статья документации.

```csharp
public abstract class DocumentVisitor
```

## Методы

| Имя | Описание |
| --- | --- |
| virtual [VisitAbsolutePositionTab](../../aspose.words/documentvisitor/visitabsolutepositiontab/)(AbsolutePositionTab) | Вызывается, когда[`AbsolutePositionTab`](../absolutepositiontab/) в документе встречается узел. |
| virtual [VisitBodyEnd](../../aspose.words/documentvisitor/visitbodyend/)(Body) | Вызывается, когда перечисление основного текстового материала в разделе закончилось. |
| virtual [VisitBodyStart](../../aspose.words/documentvisitor/visitbodystart/)(Body) | Вызывается, когда начинается перечисление основного текстового материала в разделе. |
| virtual [VisitBookmarkEnd](../../aspose.words/documentvisitor/visitbookmarkend/)(BookmarkEnd) | Вызывается, когда в документе встречается конец закладки. |
| virtual [VisitBookmarkStart](../../aspose.words/documentvisitor/visitbookmarkstart/)(BookmarkStart) | Вызывается, когда в документе встречается начало закладки. |
| virtual [VisitBuildingBlockEnd](../../aspose.words/documentvisitor/visitbuildingblockend/)(BuildingBlock) | Вызывается, когда перечисление стандартного блока завершено. |
| virtual [VisitBuildingBlockStart](../../aspose.words/documentvisitor/visitbuildingblockstart/)(BuildingBlock) | Вызывается, когда началось перечисление стандартного блока. |
| virtual [VisitCellEnd](../../aspose.words/documentvisitor/visitcellend/)(Cell) | Вызывается, когда перечисление ячейки таблицы завершено. |
| virtual [VisitCellStart](../../aspose.words/documentvisitor/visitcellstart/)(Cell) | Вызывается, когда началось перечисление ячейки таблицы. |
| virtual [VisitCommentEnd](../../aspose.words/documentvisitor/visitcommentend/)(Comment) | Вызывается, когда перечисление текста комментария завершено. |
| virtual [VisitCommentRangeEnd](../../aspose.words/documentvisitor/visitcommentrangeend/)(CommentRangeEnd) | Вызывается, когда встречается конец закомментированного диапазона текста. |
| virtual [VisitCommentRangeStart](../../aspose.words/documentvisitor/visitcommentrangestart/)(CommentRangeStart) | Вызывается, когда встречается начало закомментированного диапазона текста. |
| virtual [VisitCommentStart](../../aspose.words/documentvisitor/visitcommentstart/)(Comment) | Вызывается, когда начинается перечисление текста комментария. |
| virtual [VisitDocumentEnd](../../aspose.words/documentvisitor/visitdocumentend/)(Document) | Вызывается, когда перечисление документа завершено. |
| virtual [VisitDocumentStart](../../aspose.words/documentvisitor/visitdocumentstart/)(Document) | Вызывается, когда началось перечисление документа. |
| virtual [VisitEditableRangeEnd](../../aspose.words/documentvisitor/visiteditablerangeend/)(EditableRangeEnd) | Вызывается, когда в документе встречается конец редактируемого диапазона. |
| virtual [VisitEditableRangeStart](../../aspose.words/documentvisitor/visiteditablerangestart/)(EditableRangeStart) | Вызывается, когда в документе встречается начало редактируемого диапазона. |
| virtual [VisitFieldEnd](../../aspose.words/documentvisitor/visitfieldend/)(FieldEnd) | Вызывается, когда в документе заканчивается поле. |
| virtual [VisitFieldSeparator](../../aspose.words/documentvisitor/visitfieldseparator/)(FieldSeparator) | Вызывается, когда в документе встречается разделитель полей. |
| virtual [VisitFieldStart](../../aspose.words/documentvisitor/visitfieldstart/)(FieldStart) | Вызывается, когда в документе начинается поле. |
| virtual [VisitFootnoteEnd](../../aspose.words/documentvisitor/visitfootnoteend/)(Footnote) | Вызывается, когда перечисление текста сноски или концевой сноски завершено. |
| virtual [VisitFootnoteStart](../../aspose.words/documentvisitor/visitfootnotestart/)(Footnote) | Вызывается, когда начинается перечисление текста сноски или концевой сноски. |
| virtual [VisitFormField](../../aspose.words/documentvisitor/visitformfield/)(FormField) | Вызывается, когда в документе встречается поле формы. |
| virtual [VisitGlossaryDocumentEnd](../../aspose.words/documentvisitor/visitglossarydocumentend/)(GlossaryDocument) | Вызывается, когда перечисление документа глоссария завершено. |
| virtual [VisitGlossaryDocumentStart](../../aspose.words/documentvisitor/visitglossarydocumentstart/)(GlossaryDocument) | Вызывается, когда начинается перечисление документа глоссария. |
| virtual [VisitGroupShapeEnd](../../aspose.words/documentvisitor/visitgroupshapeend/)(GroupShape) | Вызывается, когда перечисление формы группы завершено. |
| virtual [VisitGroupShapeStart](../../aspose.words/documentvisitor/visitgroupshapestart/)(GroupShape) | Вызывается, когда началось перечисление фигуры группы. |
| virtual [VisitHeaderFooterEnd](../../aspose.words/documentvisitor/visitheaderfooterend/)(HeaderFooter) | Вызывается, когда перечисление верхнего или нижнего колонтитула в разделе закончилось. |
| virtual [VisitHeaderFooterStart](../../aspose.words/documentvisitor/visitheaderfooterstart/)(HeaderFooter) | Вызывается, когда началось перечисление верхнего или нижнего колонтитула в разделе. |
| virtual [VisitOfficeMathEnd](../../aspose.words/documentvisitor/visitofficemathend/)(OfficeMath) | Вызывается, когда перечисление объекта Office Math завершено. |
| virtual [VisitOfficeMathStart](../../aspose.words/documentvisitor/visitofficemathstart/)(OfficeMath) | Вызывается, когда начинается перечисление объекта Office Math. |
| virtual [VisitParagraphEnd](../../aspose.words/documentvisitor/visitparagraphend/)(Paragraph) | Вызывается, когда перечисление абзаца закончилось. |
| virtual [VisitParagraphStart](../../aspose.words/documentvisitor/visitparagraphstart/)(Paragraph) | Вызывается, когда начинается перечисление абзаца. |
| virtual [VisitRowEnd](../../aspose.words/documentvisitor/visitrowend/)(Row) | Вызывается, когда перечисление строки таблицы завершено. |
| virtual [VisitRowStart](../../aspose.words/documentvisitor/visitrowstart/)(Row) | Вызывается, когда начинается перечисление строки таблицы. |
| virtual [VisitRun](../../aspose.words/documentvisitor/visitrun/)(Run) | Вызывается, когда встречается текст в. |
| virtual [VisitSectionEnd](../../aspose.words/documentvisitor/visitsectionend/)(Section) | Вызывается, когда перечисление раздела завершено. |
| virtual [VisitSectionStart](../../aspose.words/documentvisitor/visitsectionstart/)(Section) | Вызывается, когда начинается перечисление раздела. |
| virtual [VisitShapeEnd](../../aspose.words/documentvisitor/visitshapeend/)(Shape) | Вызывается, когда перечисление фигуры завершено. |
| virtual [VisitShapeStart](../../aspose.words/documentvisitor/visitshapestart/)(Shape) | Вызывается, когда начинается перечисление фигуры. |
| virtual [VisitSmartTagEnd](../../aspose.words/documentvisitor/visitsmarttagend/)(SmartTag) | Вызывается, когда перечисление смарт-тега завершено. |
| virtual [VisitSmartTagStart](../../aspose.words/documentvisitor/visitsmarttagstart/)(SmartTag) | Вызывается, когда началось перечисление смарт-тега. |
| virtual [VisitSpecialChar](../../aspose.words/documentvisitor/visitspecialchar/)(SpecialChar) | Вызывается, когда[`SpecialChar`](../specialchar/) в документе встречается узел. |
| virtual [VisitStructuredDocumentTagEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagend/)(StructuredDocumentTag) | Вызывается, когда перечисление тега структурированного документа завершено. |
| virtual [VisitStructuredDocumentTagRangeEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagrangeend/)(StructuredDocumentTagRangeEnd) | Вызывается при обнаружении StructuredDocumentTagRangeEnd. |
| virtual [VisitStructuredDocumentTagRangeStart](../../aspose.words/documentvisitor/visitstructureddocumenttagrangestart/)(StructuredDocumentTagRangeStart) | Вызывается при обнаружении StructuredDocumentTagRangeStart. |
| virtual [VisitStructuredDocumentTagStart](../../aspose.words/documentvisitor/visitstructureddocumenttagstart/)(StructuredDocumentTag) | Вызывается, когда началось перечисление тега структурированного документа. |
| virtual [VisitSubDocument](../../aspose.words/documentvisitor/visitsubdocument/)(SubDocument) | Вызывается при обнаружении вложенного документа. |
| virtual [VisitTableEnd](../../aspose.words/documentvisitor/visittableend/)(Table) | Вызывается, когда перечисление таблицы завершено. |
| virtual [VisitTableStart](../../aspose.words/documentvisitor/visittablestart/)(Table) | Вызывается, когда началось перечисление таблицы. |

### Примечания

С`DocumentVisitor` вы можете определить и выполнить пользовательские операции , требующие перечисления по дереву документа.

Например, Aspose.Words использует`DocumentVisitor` внутри для экономии[`Document`](../document/) в различных форматах и для других операций, таких как поиск полей или закладок над фрагментом документа.

Использовать`DocumentVisitor`:

1. Создайте класс, производный от`DocumentVisitor`.
2. Переопределить и предоставить реализации для некоторых или всех методов VisitXXX для выполнения некоторых пользовательских операций.
3. Вызов[`Узел.Принять`](../node/accept/) на[`Node`](../node/) that , с которого вы хотите начать перечисление.

`DocumentVisitor` предоставляет реализации по умолчанию для всех методов VisitXXX , чтобы упростить создание новых посетителей документа, поскольку необходимо переопределить только методы, необходимые для конкретного посетителя . Нет необходимости переопределять все методы посетителя.

Дополнительные сведения см. в шаблоне проектирования «Посетитель».

### Примеры

Показывает, как использовать посетитель документа для печати структуры узла документа.

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // Когда мы получаем составной узел для приема посетителя документа, посетитель посещает принимающий узел,
    // а затем обходит все дочерние узлы в глубину.
    // Посетитель может читать и изменять каждый посещенный узел.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Обходит дерево дочерних узлов узла.
/// Создает карту этого дерева в виде строки.
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
    /// Вызывается при обнаружении узла Document.
    /// </summary>
    public override VisitorAction VisitDocumentStart(Document doc)
    {
        int childNodeCount = doc.GetChildNodes(NodeType.Any, true).Count;

        IndentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
        mDocTraversalDepth++;

        // Разрешить посетителю продолжить посещение других узлов.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается после посещения всех дочерних узлов узла Document.
    /// </summary>
    public override VisitorAction VisitDocumentEnd(Document doc)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Document end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел Раздела.
    /// </summary>
    public override VisitorAction VisitSectionStart(Section section)
    {
        // Получаем индекс нашего раздела в документе.
        NodeCollection docSections = section.Document.GetChildNodes(NodeType.Section, false);
        int sectionIndex = docSections.IndexOf(section);

        IndentAndAppendLine("[Section start] Section index: " + sectionIndex);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается после посещения всех дочерних узлов узла Раздела.
    /// </summary>
    public override VisitorAction VisitSectionEnd(Section section)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Section end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел Body.
    /// </summary>
    public override VisitorAction VisitBodyStart(Body body)
    {
        int paragraphCount = body.Paragraphs.Count;
        IndentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается после посещения всех дочерних узлов узла Body.
    /// </summary>
    public override VisitorAction VisitBodyEnd(Body body)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Body end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел «Абзац».
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        IndentAndAppendLine("[Paragraph start]");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается после посещения всех дочерних узлов узла Paragraph.
    /// </summary>
    public override VisitorAction VisitParagraphEnd(Paragraph paragraph)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Paragraph end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел Run.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел SubDocument.
    /// </summary>
    public override VisitorAction VisitSubDocument(SubDocument subDocument)
    {
        IndentAndAppendLine("[SubDocument]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Добавляем строку к StringBuilder и отступаем от нее в зависимости от того, насколько глубоко посетитель находится в дереве документа.
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

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


