---
title: IMailMergeCallback.TagsReplaced
linktitle: TagsReplaced
articleTitle: TagsReplaced
second_title: Aspose.Words для .NET
description: IMailMergeCallback TagsReplaced метод. Вызывается когда текстовые теги усы заменяются полями MERGEFIELD на С#.
type: docs
weight: 10
url: /ru/net/aspose.words.mailmerging/imailmergecallback/tagsreplaced/
---
## IMailMergeCallback.TagsReplaced method

Вызывается, когда текстовые теги «усы» заменяются полями MERGEFIELD.

```csharp
public void TagsReplaced()
```

## Примеры

Показывает, как определить пользовательскую логику для обработки событий во время слияния почты.

```csharp
public void Callback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Вставляем два тега слияния почты, ссылающиеся на два столбца в источнике данных.
    builder.Write("{{FirstName}}");
    builder.Write("{{LastName}}");

    // Создайте источник данных, содержащий только один из столбцов, на которые ссылаются наши теги слияния.
    DataTable table = new DataTable("Test");
    table.Columns.Add("FirstName");
    table.Rows.Add("John");
    table.Rows.Add("Jane");

    // Настройте наше слияние почты на использование альтернативных тегов слияния почты.
    doc.MailMerge.UseNonMergeFields = true;

    // Затем убедитесь, что слияние почты преобразует теги, такие как наш тег «Фамилия»,
    // в поля MERGEFIELD в документах слияния.
    doc.MailMerge.PreserveUnusedTags = false;

    MailMergeTagReplacementCounter counter = new MailMergeTagReplacementCounter();
    doc.MailMerge.MailMergeCallback = counter;
    doc.MailMerge.Execute(table);

    Assert.AreEqual(1, counter.TagsReplacedCount);
}

/// <summary>
/// Подсчитывает количество раз, когда слияние почты заменяет теги слияния почты, которые не удалось заполнить данными с помощью MERGEFIELD.
/// </summary>
private class MailMergeTagReplacementCounter : IMailMergeCallback
{
    public void TagsReplaced()
    {
        TagsReplacedCount++;
    }

    public int TagsReplacedCount { get; private set; }
}
```

### Смотрите также

* property [UseNonMergeFields](../../mailmerge/usenonmergefields/)
* interface [IMailMergeCallback](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
