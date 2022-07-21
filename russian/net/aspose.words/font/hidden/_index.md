---
title: Hidden
second_title: Справочник по API Aspose.Words для .NET
description: Истинно если шрифт отформатирован как скрытый текст.
type: docs
weight: 140
url: /ru/net/aspose.words/font/hidden/
---
## Font.Hidden property

Истинно, если шрифт отформатирован как скрытый текст.

```csharp
public bool Hidden { get; set; }
```

### Примеры

Показывает, как создать серию скрытого текста.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Если для параметра Hidden установлено значение true, любой текст, который мы создаем с помощью этого объекта Font, будет невидим в документе.
// Мы не будем видеть или выделять скрытый текст, пока не включим опцию «Скрытый текст»
// найти в Microsoft Word через "Файл" -> "Опции" -> "Отображать". Текст все равно будет там,
// и мы сможем получить доступ к этому тексту программно.
// Не рекомендуется использовать этот метод для сокрытия конфиденциальной информации.
builder.Font.Hidden = true;
builder.Font.Size = 36;

builder.Writeln("This text will not be visible in the document.");

doc.Save(ArtifactsDir + "Font.Hidden.docx");
```

Показывает, как использовать реализацию DocumentVisitor для удаления всего скрытого содержимого из документа.

```csharp
{
    Document doc = new Document(MyDir + "Hidden content.docx");

    RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

    // Ниже приведены три типа полей, которые могут принять посетителя документа,
    // что позволит ему посетить принимающий узел, а затем пройти его дочерние узлы в порядке глубины.
    // 1 - Узел абзаца:
    Paragraph para = (Paragraph) doc.GetChild(NodeType.Paragraph, 4, true);
    para.Accept(hiddenContentRemover);

    // 2 - Узел таблицы:
    Table table = doc.FirstSection.Body.Tables[0];
    table.Accept(hiddenContentRemover);

    // 3 - Узел документа:
    doc.Accept(hiddenContentRemover);

    doc.Save(ArtifactsDir + "Font.RemoveHiddenContentFromDocument.docx");

/// <summary>
/// Удаляет все посещенные узлы, помеченные как "скрытый контент".
/// </summary>
public class RemoveHiddenContentVisitor : DocumentVisitor
{
    /// <summary>
    /// Вызывается, когда в документе встречается узел FieldStart.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        if (fieldStart.Font.Hidden)
            fieldStart.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел FieldEnd.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.Font.Hidden)
            fieldEnd.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел FieldSeparator.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        if (fieldSeparator.Font.Hidden)
            fieldSeparator.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел Run.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (run.Font.Hidden)
            run.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел Paragraph.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        if (paragraph.ParagraphBreakFont.Hidden)
            paragraph.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается FormField.
    /// </summary>
    public override VisitorAction VisitFormField(FormField formField)
    {
        if (formField.Font.Hidden)
            formField.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается GroupShape.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        if (groupShape.Font.Hidden)
            groupShape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается фигура.
    /// </summary>
    public override VisitorAction VisitShapeStart(Shape shape)
    {
        if (shape.Font.Hidden)
            shape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается комментарий.
    /// </summary>
    public override VisitorAction VisitCommentStart(Comment comment)
    {
        if (comment.Font.Hidden)
            comment.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается сноска.
    /// </summary>
    public override VisitorAction VisitFootnoteStart(Footnote footnote)
    {
        if (footnote.Font.Hidden)
            footnote.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается SpecialCharacter.
    /// </summary>
    public override VisitorAction VisitSpecialChar(SpecialChar specialChar)
    {
        if (specialChar.Font.Hidden)
            specialChar.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается при завершении посещения узла Table в документе.
    /// </summary>
    public override VisitorAction VisitTableEnd(Table table)
    {
        // Содержимое внутри ячеек таблицы может иметь флаг скрытого содержимого, но не сами таблицы.
        // Если бы в этой таблице не было ничего, кроме скрытого содержимого, этот посетитель удалил бы все это,
        // и не осталось бы дочерних узлов.
        // Таким образом, мы также можем рассматривать саму таблицу как скрытое содержимое и удалять ее.
        // Таблицы, которые пусты, но не имеют скрытого содержимого, будут иметь ячейки с пустыми абзацами внутри,
        // который этот посетитель не удалит.
        if (!table.HasChildNodes)
            table.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается при завершении посещения узла Cell в документе.
    /// </summary>
    public override VisitorAction VisitCellEnd(Cell cell)
    {
        if (!cell.HasChildNodes && cell.ParentNode != null)
            cell.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается при завершении посещения узла Row в документе.
    /// </summary>
    public override VisitorAction VisitRowEnd(Row row)
    {
        if (!row.HasChildNodes && row.ParentNode != null)
            row.Remove();

        return VisitorAction.Continue;
    }
}
```

### Смотрите также

* class [Font](../../font)
* пространство имен [Aspose.Words](../../font)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
