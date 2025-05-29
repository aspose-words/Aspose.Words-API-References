---
title: DocumentVisitor.VisitAbsolutePositionTab
linktitle: VisitAbsolutePositionTab
articleTitle: VisitAbsolutePositionTab
second_title: Aspose.Words для .NET
description: Откройте для себя метод DocumentVisitor VisitAbsolutePositionTab, разработанный для улучшения обработки документов за счет эффективной обработки узлов AbsolutePositionTab.
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
| tab | AbsolutePositionTab | Посещаемый объект. |

### Возвращаемое значение

А[`VisitorAction`](../../visitoraction/) значение, указывающее, как продолжить перечисление.

## Примеры

Показывает, как обрабатывать символы табуляции абсолютного положения с помощью посетителя документа.

```csharp
public void DocumentToTxt()
{
    Document doc = new Document(MyDir + "Absolute position tab.docx");

    // Извлекаем текстовое содержимое нашего документа, приняв этого посетителя пользовательского документа.
    DocTextExtractor myDocTextExtractor = new DocTextExtractor();
    Section fisrtSection = doc.FirstSection;
    fisrtSection.Body.Accept(myDocTextExtractor);
    // Посетить только начало тела документа.
    fisrtSection.Body.AcceptStart(myDocTextExtractor);
    // Посетить только конец тела документа.
    fisrtSection.Body.AcceptEnd(myDocTextExtractor);

    // Абсолютная позиция табуляции, не имеющая эквивалента в строковой форме, была явно преобразована в символ табуляции.
    Assert.AreEqual("Before AbsolutePositionTab\tAfter AbsolutePositionTab", myDocTextExtractor.GetText());

    // AbsolutePositionTab также может принимать DocumentVisitor самостоятельно.
    AbsolutePositionTab absPositionTab = (AbsolutePositionTab)doc.FirstSection.Body.FirstParagraph.GetChild(NodeType.SpecialChar, 0, true);

    myDocTextExtractor = new DocTextExtractor();
    absPositionTab.Accept(myDocTextExtractor);

    Assert.AreEqual("\t", myDocTextExtractor.GetText());
}

/// <summary>
/// Собирает текстовое содержимое всех прогонов в посещенном документе. Заменяет все абсолютные символы табуляции на обычные табуляции.
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
    /// Добавляет текст к текущему выводу. Учитывает флаг включенного/отключенного вывода.
    /// </summary>
    private void AppendText(string text)
    {
        mBuilder.Append(text);
    }

    /// <summary>
    /// Простой текст документа, накопленный посетителем.
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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
