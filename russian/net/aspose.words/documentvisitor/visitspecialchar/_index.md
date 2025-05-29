---
title: DocumentVisitor.VisitSpecialChar
linktitle: VisitSpecialChar
articleTitle: VisitSpecialChar
second_title: Aspose.Words для .NET
description: Узнайте, как метод DocumentVisitor VisitSpecialChar улучшает обработку документов за счет эффективной обработки узлов SpecialChar для повышения производительности.
type: docs
weight: 430
url: /ru/net/aspose.words/documentvisitor/visitspecialchar/
---
## DocumentVisitor.VisitSpecialChar method

Вызывается, когда[`SpecialChar`](../../specialchar/) узел встречается в документе.

```csharp
public virtual VisitorAction VisitSpecialChar(SpecialChar specialChar)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| specialChar | SpecialChar | Посещаемый объект. |

### Возвращаемое значение

А[`VisitorAction`](../../visitoraction/) значение, указывающее, как продолжить перечисление.

## Примечания

Этот метод не вызывается для универсальных управляющих символов (см.[`ControlChar`](../../controlchar/) ), которые могут присутствовать в документе.

## Примеры

Показывает, как использовать реализацию DocumentVisitor для удаления всего скрытого содержимого из документа.

```csharp
public void RemoveHiddenContentFromDocument()
{
    Document doc = new Document(MyDir + "Hidden content.docx");
    RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

    // Ниже приведены три типа полей, которые могут принять посетителя документа,
    // что позволит ему посетить принимающий узел, а затем обойти его дочерние узлы в глубину.
    // 1 - Узел абзаца:
    Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 4, true);
    para.Accept(hiddenContentRemover);

    // 2 - Узел таблицы:
    Table table = doc.FirstSection.Body.Tables[0];
    table.Accept(hiddenContentRemover);

    // 3 - Узел документа:
    doc.Accept(hiddenContentRemover);

    doc.Save(ArtifactsDir + "Font.RemoveHiddenContentFromDocument.docx");
}

/// <summary>
/// Удаляет все посещенные узлы, отмеченные как «скрытое содержимое».
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
    /// Вызывается, когда в документе встречается узел «Абзац».
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
    /// Вызывается при обнаружении фигуры в документе.
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
    /// Вызывается, когда в документе встречается специальный символ.
    /// </summary>
    public override VisitorAction VisitSpecialChar(SpecialChar specialChar)
    {
        Console.WriteLine(specialChar.GetText());

        if (specialChar.Font.Hidden)
            specialChar.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда посещение узла таблицы в документе завершено.
    /// </summary>
    public override VisitorAction VisitTableEnd(Table table)
    {
        // Содержимое ячеек таблицы может иметь флаг скрытого содержимого, но сами таблицы — нет.
        // Если бы в этой таблице не было ничего, кроме скрытого контента, этот посетитель удалил бы его весь,
        // и не останется ни одного дочернего узла.
        // Таким образом, мы также можем рассматривать саму таблицу как скрытое содержимое и удалить ее.
        // Таблицы, которые пусты, но не имеют скрытого содержимого, будут иметь ячейки с пустыми абзацами внутри,
        // который этот посетитель не удалит.
        if (!table.HasChildNodes)
            table.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда посещение узла ячейки в документе завершено.
    /// </summary>
    public override VisitorAction VisitCellEnd(Cell cell)
    {
        if (!cell.HasChildNodes && cell.ParentNode != null)
            cell.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда посещение узла строки в документе завершено.
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

* enum [VisitorAction](../../visitoraction/)
* class [SpecialChar](../../specialchar/)
* class [DocumentVisitor](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
