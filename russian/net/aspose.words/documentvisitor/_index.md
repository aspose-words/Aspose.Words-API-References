---
title: DocumentVisitor
second_title: Справочник по API Aspose.Words для .NET
description: Базовый класс для пользовательских посетителей документов.
type: docs
weight: 460
url: /ru/net/aspose.words/documentvisitor/
---
## DocumentVisitor class

Базовый класс для пользовательских посетителей документов.

```csharp
public abstract class DocumentVisitor
```

## Методы

| Имя | Описание |
| --- | --- |
| virtual [VisitAbsolutePositionTab](../../aspose.words/documentvisitor/visitabsolutepositiontab)(AbsolutePositionTab) | Вызывается, когда в документе встречается узел[`AbsolutePositionTab`](../absolutepositiontab). |
| virtual [VisitBodyEnd](../../aspose.words/documentvisitor/visitbodyend)(Body) | Вызывается, когда закончился перебор основного текста в разделе. |
| virtual [VisitBodyStart](../../aspose.words/documentvisitor/visitbodystart)(Body) | Вызывается, когда начался перебор основного текста в разделе. |
| virtual [VisitBookmarkEnd](../../aspose.words/documentvisitor/visitbookmarkend)(BookmarkEnd) | Вызывается, когда в документе встречается конец закладки. |
| virtual [VisitBookmarkStart](../../aspose.words/documentvisitor/visitbookmarkstart)(BookmarkStart) | Вызывается, когда в документе встречается начало закладки. |
| virtual [VisitBuildingBlockEnd](../../aspose.words/documentvisitor/visitbuildingblockend)(BuildingBlock) | Вызывается по окончании перечисления строительного блока. |
| virtual [VisitBuildingBlockStart](../../aspose.words/documentvisitor/visitbuildingblockstart)(BuildingBlock) | Вызывается, когда начинается перечисление строительного блока. |
| virtual [VisitCellEnd](../../aspose.words/documentvisitor/visitcellend)(Cell) | Вызывается, когда закончилось перечисление ячейки таблицы. |
| virtual [VisitCellStart](../../aspose.words/documentvisitor/visitcellstart)(Cell) | Вызывается при начале перечисления ячейки таблицы. |
| virtual [VisitCommentEnd](../../aspose.words/documentvisitor/visitcommentend)(Comment) | Вызывается, когда закончилось перечисление текста комментария. |
| virtual [VisitCommentRangeEnd](../../aspose.words/documentvisitor/visitcommentrangeend)(CommentRangeEnd) | Вызывается, когда встречается конец прокомментированного диапазона текста. |
| virtual [VisitCommentRangeStart](../../aspose.words/documentvisitor/visitcommentrangestart)(CommentRangeStart) | Вызывается, когда встречается начало прокомментированного диапазона текста. |
| virtual [VisitCommentStart](../../aspose.words/documentvisitor/visitcommentstart)(Comment) | Вызывается при начале перечисления текста комментария. |
| virtual [VisitDocumentEnd](../../aspose.words/documentvisitor/visitdocumentend)(Document) | Вызывается после завершения перечисления документа. |
| virtual [VisitDocumentStart](../../aspose.words/documentvisitor/visitdocumentstart)(Document) | Вызывается, когда начинается перечисление документа. |
| virtual [VisitEditableRangeEnd](../../aspose.words/documentvisitor/visiteditablerangeend)(EditableRangeEnd) | Вызывается, когда в документе встречается конец редактируемого диапазона. |
| virtual [VisitEditableRangeStart](../../aspose.words/documentvisitor/visiteditablerangestart)(EditableRangeStart) | Вызывается, когда в документе встречается начало редактируемого диапазона. |
| virtual [VisitFieldEnd](../../aspose.words/documentvisitor/visitfieldend)(FieldEnd) | Вызывается, когда в документе заканчивается поле. |
| virtual [VisitFieldSeparator](../../aspose.words/documentvisitor/visitfieldseparator)(FieldSeparator) | Вызывается, когда в документе встречается разделитель полей. |
| virtual [VisitFieldStart](../../aspose.words/documentvisitor/visitfieldstart)(FieldStart) | Вызывается, когда в документе начинается поле. |
| virtual [VisitFootnoteEnd](../../aspose.words/documentvisitor/visitfootnoteend)(Footnote) | Вызывается, когда закончилось перечисление текста сноски или концевой сноски. |
| virtual [VisitFootnoteStart](../../aspose.words/documentvisitor/visitfootnotestart)(Footnote) | Вызывается, когда начинается перечисление текста сноски или концевой сноски. |
| virtual [VisitFormField](../../aspose.words/documentvisitor/visitformfield)(FormField) | Вызывается, когда в документе встречается поле формы. |
| virtual [VisitGlossaryDocumentEnd](../../aspose.words/documentvisitor/visitglossarydocumentend)(GlossaryDocument) | Вызывается, когда закончилось перечисление документа глоссария. |
| virtual [VisitGlossaryDocumentStart](../../aspose.words/documentvisitor/visitglossarydocumentstart)(GlossaryDocument) | Вызывается, когда начинается перечисление документа глоссария. |
| virtual [VisitGroupShapeEnd](../../aspose.words/documentvisitor/visitgroupshapeend)(GroupShape) | Вызывается, когда закончилось перечисление формы группы. |
| virtual [VisitGroupShapeStart](../../aspose.words/documentvisitor/visitgroupshapestart)(GroupShape) | Вызывается, когда начинается перечисление формы группы. |
| virtual [VisitHeaderFooterEnd](../../aspose.words/documentvisitor/visitheaderfooterend)(HeaderFooter) | Вызывается, когда закончилось перечисление верхнего или нижнего колонтитула в разделе. |
| virtual [VisitHeaderFooterStart](../../aspose.words/documentvisitor/visitheaderfooterstart)(HeaderFooter) | Вызывается, когда начинается перечисление верхнего или нижнего колонтитула в разделе. |
| virtual [VisitOfficeMathEnd](../../aspose.words/documentvisitor/visitofficemathend)(OfficeMath) | Вызывается после завершения перечисления объекта Office Math. |
| virtual [VisitOfficeMathStart](../../aspose.words/documentvisitor/visitofficemathstart)(OfficeMath) | Вызывается при запуске перечисления объекта Office Math. |
| virtual [VisitParagraphEnd](../../aspose.words/documentvisitor/visitparagraphend)(Paragraph) | Вызывается, когда закончилось перечисление абзаца. |
| virtual [VisitParagraphStart](../../aspose.words/documentvisitor/visitparagraphstart)(Paragraph) | Вызывается при начале перечисления абзаца. |
| virtual [VisitRowEnd](../../aspose.words/documentvisitor/visitrowend)(Row) | Вызывается, когда закончилось перечисление строки таблицы. |
| virtual [VisitRowStart](../../aspose.words/documentvisitor/visitrowstart)(Row) | Вызывается, когда начинается перечисление строки таблицы. |
| virtual [VisitRun](../../aspose.words/documentvisitor/visitrun)(Run) | Вызывается при обнаружении фрагмента текста в . |
| virtual [VisitSectionEnd](../../aspose.words/documentvisitor/visitsectionend)(Section) | Вызывается, когда закончилось перечисление секции. |
| virtual [VisitSectionStart](../../aspose.words/documentvisitor/visitsectionstart)(Section) | Вызывается при начале перечисления секции. |
| virtual [VisitShapeEnd](../../aspose.words/documentvisitor/visitshapeend)(Shape) | Вызывается, когда закончилось перечисление формы. |
| virtual [VisitShapeStart](../../aspose.words/documentvisitor/visitshapestart)(Shape) | Вызывается, когда начинается перечисление формы. |
| virtual [VisitSmartTagEnd](../../aspose.words/documentvisitor/visitsmarttagend)(SmartTag) | Вызывается, когда закончилось перечисление смарт-тега. |
| virtual [VisitSmartTagStart](../../aspose.words/documentvisitor/visitsmarttagstart)(SmartTag) | Вызывается, когда начинается перечисление смарт-тега. |
| virtual [VisitSpecialChar](../../aspose.words/documentvisitor/visitspecialchar)(SpecialChar) | Вызывается, когда в документе встречается узел[`SpecialChar`](../specialchar). |
| virtual [VisitStructuredDocumentTagEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagend)(StructuredDocumentTag) | Вызывается, когда закончилось перечисление тега структурированного документа. |
| virtual [VisitStructuredDocumentTagRangeEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagrangeend)(StructuredDocumentTagRangeEnd) |  |
| virtual [VisitStructuredDocumentTagRangeStart](../../aspose.words/documentvisitor/visitstructureddocumenttagrangestart)(StructuredDocumentTagRangeStart) |  |
| virtual [VisitStructuredDocumentTagStart](../../aspose.words/documentvisitor/visitstructureddocumenttagstart)(StructuredDocumentTag) | Вызывается, когда начинается перечисление тега структурированного документа. |
| virtual [VisitSubDocument](../../aspose.words/documentvisitor/visitsubdocument)(SubDocument) | Вызывается при обнаружении вложенного документа. |
| virtual [VisitTableEnd](../../aspose.words/documentvisitor/visittableend)(Table) | Вызывается, когда закончилось перечисление таблицы. |
| virtual [VisitTableStart](../../aspose.words/documentvisitor/visittablestart)(Table) | Вызывается при начале перечисления таблицы. |

### Примечания

С **DocumentVisitor** вы может определять и выполнять пользовательские операции , которые требуют перечисления по дереву документа.

Например, Aspose.Words использует **DocumentVisitor** для внутреннего сохранения **Document** в различных форматах и для других операций вроде поиска полей или закладок над фрагментом документа.

Для использования **DocumentVisitor** :

1. Создайте класс, производный от **DocumentVisitor** .
2. Переопределить и предоставить реализации для некоторых или всех методов VisitXXX для выполнения некоторых пользовательских операций.
3. Call[`Node.Accept`](../node/accept) на узле , с которого вы хотите начать перечисление.

**DocumentVisitor** предоставляет реализации по умолчанию для всех методов VisitXXX для упрощения создания новых посетителей документа, поскольку необходимо переопределить только методы, необходимые для конкретного посетителя. Нет необходимости переопределять все методы посетителя.

Дополнительные сведения см. в шаблоне проектирования "Посетитель".

### Примеры

Показывает, как использовать посетитель документа для печати структуры узла документа.

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

     // Когда составной узел принимает посетителя документа, посетитель посещает принимающий узел, 
     // а затем обходит все дочерние узлы в порядке глубины.
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
     /// Вызывается, когда в документе встречается узел Section.
    /// </summary>
    public override VisitorAction VisitSectionStart(Section section)
    {
         // Получаем индекс нашего раздела внутри документа.
        NodeCollection docSections = section.Document.GetChildNodes(NodeType.Section, false);
        int sectionIndex = docSections.IndexOf(section);

        IndentAndAppendLine("[Section start] Section index: " + sectionIndex);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
     /// Вызывается после посещения всех дочерних узлов узла Section.
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
     /// Вызывается, когда в документе встречается узел Paragraph.
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
     /// Добавляем строку в StringBuilder и делаем отступ в зависимости от того, насколько глубоко посетитель находится в дереве документа.
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

* пространство имен [Aspose.Words](../../aspose.words)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
