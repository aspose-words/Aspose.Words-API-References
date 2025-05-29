---
title: VisitorAction Enum
linktitle: VisitorAction
articleTitle: VisitorAction
second_title: Aspose.Words для .NET
description: Изучите перечисление Aspose.Words.VisitorAction, чтобы легко управлять перечислением узлов, повышая эффективность и контроль обработки документов.
type: docs
weight: 7470
url: /ru/net/aspose.words/visitoraction/
---
## VisitorAction enumeration

Позволяет посетителю управлять перечислением узлов.

```csharp
public enum VisitorAction
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Continue | `0` | Посетитель запрашивает продолжение перечисления. |
| SkipThisNode | `1` | Посетитель запрашивает пропуск текущего узла и продолжение перечисления. |
| Stop | `2` | Посетитель запрашивает остановку перечисления узлов. |

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
