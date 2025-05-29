---
title: IMailMergeCallback.TagsReplaced
linktitle: TagsReplaced
articleTitle: TagsReplaced
second_title: Aspose.Words для .NET
description: Узнайте, как метод IMailMergeCallback TagsReplaced улучшает автоматизацию документов, легко заменяя текст «усы» полями MERGEFIELD.
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

    // Вставьте два тега слияния почты, ссылающихся на два столбца в источнике данных.
    builder.Write("{{FirstName}}");
    builder.Write("{{LastName}}");

    // Создайте источник данных, содержащий только один из столбцов, на которые ссылаются наши теги слияния.
    DataTable table = new DataTable("Test");
    table.Columns.Add("FirstName");
    table.Rows.Add("John");
    table.Rows.Add("Jane");

    // Настройте наше слияние почты для использования альтернативных тегов слияния почты.
    doc.MailMerge.UseNonMergeFields = true;

    // Затем убедитесь, что слияние преобразует теги, такие как наш тег «LastName»,
    // в поля MERGEFIELD в документах слияния.
    doc.MailMerge.PreserveUnusedTags = false;

    MailMergeTagReplacementCounter counter = new MailMergeTagReplacementCounter();
    doc.MailMerge.MailMergeCallback = counter;
    doc.MailMerge.Execute(table);

    Assert.AreEqual(1, counter.TagsReplacedCount);
}

/// <summary>
/// Подсчитывает количество раз, когда слияние почты заменяет теги слияния почты, которые оно не смогло заполнить данными с помощью MERGEFIELD.
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
