---
title: Body.AcceptStart
linktitle: AcceptStart
articleTitle: AcceptStart
second_title: Aspose.Words для .NET
description: Откройте для себя метод Body AcceptStart, который позволяет легко интегрировать посетителей в начало текста документа для улучшения пользовательского опыта.
type: docs
weight: 60
url: /ru/net/aspose.words/body/acceptstart/
---
## Body.AcceptStart method

Принимает посетителя для посещения начала тела документа.

```csharp
public override VisitorAction AcceptStart(DocumentVisitor visitor)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| visitor | DocumentVisitor | Посетитель документа. |

### Возвращаемое значение

Действие, которое должен предпринять посетитель.

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
* class [DocumentVisitor](../../documentvisitor/)
* class [Body](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
