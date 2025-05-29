---
title: FindReplaceOptions.UseLegacyOrder
linktitle: UseLegacyOrder
articleTitle: UseLegacyOrder
second_title: Aspose.Words для .NET
description: Откройте для себя свойство UseLegacyOrder в FindReplaceOptions. Включите последовательный текстовый поиск для большей точности. Значение по умолчанию — false. Оптимизируйте обработку текста!
type: docs
weight: 180
url: /ru/net/aspose.words.replacing/findreplaceoptions/uselegacyorder/
---
## FindReplaceOptions.UseLegacyOrder property

True указывает, что поиск текста выполняется последовательно сверху вниз с учетом текстовых полей. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool UseLegacyOrder { get; set; }
```

## Примеры

Показывает, как изменить порядок поиска узлов при выполнении операции поиска и замены текста.

```csharp
public void UseLegacyOrder(bool useLegacyOrder)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Вставляем три записи, которые можно искать с помощью шаблона регулярного выражения.
    // Поместите один из этих фрагментов в текстовое поле.
    builder.Writeln("[tag 1]");
    Shape textBox = builder.InsertShape(ShapeType.TextBox, 100, 50);
    builder.Writeln("[tag 2]");
    builder.MoveTo(textBox.FirstParagraph);
    builder.Write("[tag 3]");

    // Мы можем использовать объект «FindReplaceOptions» для изменения процесса поиска и замены.
    FindReplaceOptions options = new FindReplaceOptions();

    // Назначаем пользовательский обратный вызов свойству "ReplacingCallback".
    TextReplacementTracker callback = new TextReplacementTracker();
    options.ReplacingCallback = callback;

    // Если мы установим свойство "UseLegacyOrder" в значение "true",
    // операция поиска и замены будет проходить по всем фрагментам за пределами текстового поля
    // прежде чем переходить к тем, что находятся внутри текстового поля.
    // Если мы установим свойство "UseLegacyOrder" в значение "false",
    // операция поиска и замены будет последовательно обрабатывать все фрагменты в диапазоне.
    options.UseLegacyOrder = useLegacyOrder;

    doc.Range.Replace(new Regex(@"\[tag \d*\]"), "", options);

    Assert.AreEqual(useLegacyOrder ?
        new List<string> { "[tag 1]", "[tag 3]", "[tag 2]" } :
        new List<string> { "[tag 1]", "[tag 2]", "[tag 3]" }, callback.Matches);
}

/// <summary>
/// Записывает порядок всех совпадений, которые встречаются во время операции поиска и замены.
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
