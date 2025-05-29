---
title: DocumentVisitor.VisitFieldStart
linktitle: VisitFieldStart
articleTitle: VisitFieldStart
second_title: Aspose.Words для .NET
description: Откройте для себя метод DocumentVisitor VisitFieldStart, который запускается в начале поля в документе, повышая эффективность кодирования и рабочего процесса.
type: docs
weight: 200
url: /ru/net/aspose.words/documentvisitor/visitfieldstart/
---
## DocumentVisitor.VisitFieldStart method

Вызывается, когда в документе начинается поле.

```csharp
public virtual VisitorAction VisitFieldStart(FieldStart fieldStart)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldStart | FieldStart | Посещаемый объект. |

### Возвращаемое значение

А[`VisitorAction`](../../visitoraction/) значение, указывающее, как продолжить перечисление.

## Примечания

Поле в документе Word состоит из кода поля и значения поля.

Например, поле, отображающее номер страницы, можно представить следующим образом:

[НачалоПоля]СТРАНИЦА[РазделительПолей]98[КонецПоля]

Разделитель полей отделяет код поля от значения поля в документе. Обратите внимание, что некоторые поля имеют только код поля и не имеют разделителя полей и значения поля.

Поля могут быть вложенными.

## Примеры

Показывает, как распечатать структуру узлов каждого поля в документе.

```csharp
public void FieldToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    FieldStructurePrinter visitor = new FieldStructurePrinter();

    // Когда мы заставляем составной узел принять посетителя документа, посетитель посещает принимающий узел,
    // а затем обходит все дочерние узлы в глубину.
    // Посетитель может читать и изменять каждый посещенный узел.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Обходит недвоичное дерево дочерних узлов узла.
/// Создает карту в виде строки всех встреченных узлов полей и их дочерних элементов.
/// </summary>
public class FieldStructurePrinter : DocumentVisitor
{
    public FieldStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideField = false;
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел Run.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideField) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел FieldStart.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        IndentAndAppendLine("[Field start] FieldType: " + fieldStart.FieldType);
        mDocTraversalDepth++;
        mVisitorIsInsideField = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел FieldEnd.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Field end]");
        mVisitorIsInsideField = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел FieldSeparator.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        IndentAndAppendLine("[FieldSeparator]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Добавляем строку в StringBuilder и делаем отступ в зависимости от того, насколько глубоко находится посетитель
    /// в дерево дочерних узлов поля.
    /// </summary>
    /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++)
        {
            mBuilder.Append("|  ");
        }

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideField;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Смотрите также

* enum [VisitorAction](../../visitoraction/)
* class [FieldStart](../../../aspose.words.fields/fieldstart/)
* class [DocumentVisitor](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
