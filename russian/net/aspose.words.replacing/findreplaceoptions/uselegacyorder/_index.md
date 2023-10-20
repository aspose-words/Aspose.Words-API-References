---
title: FindReplaceOptions.UseLegacyOrder
linktitle: UseLegacyOrder
articleTitle: UseLegacyOrder
second_title: Aspose.Words для .NET
description: FindReplaceOptions UseLegacyOrder свойство. True указывает что текстовый поиск выполняется последовательно сверху вниз с учетом текстовых полей. Значение по умолчаниюЛОЖЬ  на С#.
type: docs
weight: 170
url: /ru/net/aspose.words.replacing/findreplaceoptions/uselegacyorder/
---
## FindReplaceOptions.UseLegacyOrder property

True указывает, что текстовый поиск выполняется последовательно сверху вниз с учетом текстовых полей. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool UseLegacyOrder { get; set; }
```

## Примеры

Показывает, как изменить порядок поиска узлов при выполнении текстовой операции поиска и замены.

```csharp
public void UseLegacyOrder(bool useLegacyOrder)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Вставляем три прогона, которые мы можем найти, используя шаблон регулярного выражения.
    // Поместите один из этих запусков в текстовое поле.
    builder.Writeln("[tag 1]");
    Shape textBox = builder.InsertShape(ShapeType.TextBox, 100, 50);
    builder.Writeln("[tag 2]");
    builder.MoveTo(textBox.FirstParagraph);
    builder.Write("[tag 3]");

    // Мы можем использовать объект «FindReplaceOptions» для изменения процесса поиска и замены.
    FindReplaceOptions options = new FindReplaceOptions();

    // Назначаем собственный обратный вызов свойству «ReplacingCallback».
    TextReplacementTracker callback = new TextReplacementTracker();
    options.ReplacingCallback = callback;

    // Если мы установим для свойства UseLegacyOrder значение «true»,
    // операция поиска и замены пройдет через все прогоны за пределами текстового поля
    // перед тем, как перейти к тем, что находятся внутри текстового поля.
    // Если мы установим для свойства UseLegacyOrder значение «false»,
    // Операция поиска и замены будет проходить по всем пробегам в диапазоне в последовательном порядке.
    options.UseLegacyOrder = useLegacyOrder;

    doc.Range.Replace(new Regex(@"\[tag \d*\]"), "", options);

    Assert.AreEqual(useLegacyOrder ?
        new List<string> { "[tag 1]", "[tag 3]", "[tag 2]" } :
        new List<string> { "[tag 1]", "[tag 2]", "[tag 3]" }, callback.Matches);
}

/// <summary>
/// Записывает порядок всех совпадений, возникающих во время операции поиска и замены.
/// </summary>
private class TextReplacementTracker : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs e)
    {
        Matches.Add(e.Match.Value);
        return ReplaceAction.Replace;
    }

    public List<string> Matches { get; } = new List<string>();
}
```

### Смотрите также

* class [FindReplaceOptions](../)
* пространство имен [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* сборка [Aspose.Words](../../../)
