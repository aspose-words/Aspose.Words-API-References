---
title: DocumentVisitor.VisitAbsolutePositionTab
second_title: Справочник по API Aspose.Words для .NET
description: DocumentVisitor метод. Вызывается когдаAbsolutePositionTab узел встречается в документе.
type: docs
weight: 10
url: /ru/net/aspose.words/documentvisitor/visitabsolutepositiontab/
---
## DocumentVisitor.VisitAbsolutePositionTab method

Вызывается, когда[`AbsolutePositionTab`](../../absolutepositiontab/) узел встречается в документе.

```csharp
public virtual VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| tab | AbsolutePositionTab | Объект, который посещается. |

### Возвращаемое значение

А[`VisitorAction`](../../visitoraction/) значение, указывающее, как продолжить перечисление.

### Примеры

Показывает, как обрабатывать символы табуляции абсолютной позиции с помощью посетителя документа.

```csharp
public void DocumentToTxt()
{
    Document doc = new Document(MyDir + "Absolute position tab.docx");

    // Извлеките текстовое содержимое нашего документа, приняв этого пользовательского посетителя документа.
    DocTextExtractor myDocTextExtractor = new DocTextExtractor();
    doc.FirstSection.Body.Accept(myDocTextExtractor);

    // Табуляция с абсолютной позицией, не имеющая эквивалента в строковой форме, была явно преобразована в символ табуляции.
    Assert.AreEqual("Before AbsolutePositionTab\tAfter AbsolutePositionTab", myDocTextExtractor.GetText());

    // AbsolutePositionTab также может принимать DocumentVisitor сам по себе.
    AbsolutePositionTab absPositionTab = (AbsolutePositionTab)doc.FirstSection.Body.FirstParagraph.GetChild(NodeType.SpecialChar, 0, true);

    myDocTextExtractor = new DocTextExtractor();
    absPositionTab.Accept(myDocTextExtractor);

    Assert.AreEqual("\t", myDocTextExtractor.GetText());
}

/// <summary>
/// Собирает текстовое содержимое всех прогонов в посещаемом документе. Заменяет все символы абсолютной табуляции на обычные табуляции.
/// </summary>
public class DocTextExtractor : DocumentVisitor
{
    public DocTextExtractor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел Run.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        AppendText(run.Text);
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел AbsolutePositionTab.
    /// </summary>
    public override VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
    {
        mBuilder.Append("\t");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Добавляет текст к текущему выводу. Учитывает включенный/отключенный выходной флаг.
    /// </summary>
    private void AppendText(string text)
    {
        mBuilder.Append(text);
    }

    /// <summary>
    /// Простой текст документа, который накопил посетитель.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### Смотрите также

* enum [VisitorAction](../../visitoraction/)
* class [AbsolutePositionTab](../../absolutepositiontab/)
* class [DocumentVisitor](../)
* пространство имен [Aspose.Words](../../documentvisitor/)
* сборка [Aspose.Words](../../../)


