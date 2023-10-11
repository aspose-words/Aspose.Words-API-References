---
title: MailMerge.UseNonMergeFields
second_title: Справочник по API Aspose.Words для .NET
description: MailMerge свойство. Когдаистинный  указывает что помимо полей MERGEFIELD слияние почты выполняется с некоторыми другими типами полей и также с тегами fieldName.
type: docs
weight: 150
url: /ru/net/aspose.words.mailmerging/mailmerge/usenonmergefields/
---
## MailMerge.UseNonMergeFields property

Когда`истинный` , указывает, что помимо полей MERGEFIELD слияние почты выполняется с некоторыми другими типами полей и также с тегами "{{fieldName}}".

```csharp
public bool UseNonMergeFields { get; set; }
```

### Примечания

Обычно слияние почты выполняется только в полях MERGEFIELD, но у некоторых клиентов отчеты report были созданы с использованием других полей, и многие документы были созданы таким образом. Для упрощения миграции (и поскольку подход this независимо использовался несколькими клиентами) была введена возможность слияния почты в другие поля.

Когда`UseNonMergeFields` установлено на`истинный`, Aspose.Words выполнит объединение почты в следующие поля:

Имя поля MERGEFIELD

MACROBUTTON NOMACRO Имя поля

ЕСЛИ 0 = 0 "{FieldName}" ""

Кроме того, когда`UseNonMergeFields` установлено на`истинный`, Aspose.Words выполнит объединение почты в текстовые tags "{{fieldName}}". Это не поля, а просто текстовые теги.

### Примеры

Показывает, как сохранить внешний вид альтернативных тегов слияния почты, которые не используются во время слияния почты.

```csharp
public void PreserveUnusedTags(bool preserveUnusedTags)
{
    Document doc = CreateSourceDocWithAlternativeMergeFields();
    DataTable dataTable = CreateSourceTablePreserveUnusedTags();

     // По умолчанию слияние почты помещает данные из каждой строки таблицы в поля MERGEFIELD, которые именуют столбцы в этой таблице.
    // В нашем документе нет таких полей, но есть теги открытого текста, заключенные в фигурные скобки.
    // Если мы установим для флага «PreserveUnusedTags» значение «true», мы сможем рассматривать эти теги как поля MERGEFIELD.
    // чтобы позволить нашему слиянию почты вставлять данные из источника данных в эти теги.
    // Если мы установим флаг «PreserveUnusedTags» в значение «false»,
    // слияние почты преобразует эти теги в поля MERGEFIELD и оставит их незаполненными.
    doc.MailMerge.PreserveUnusedTags = preserveUnusedTags;
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.PreserveUnusedTags.docx");

    // В нашем документе есть тег для столбца с именем «Столбец2», которого нет в таблице.
    // Если мы установим флаг «PreserveUnusedTags» в значение «false», then the mail merge will convert this tag into a MERGEFIELD.
    Assert.AreEqual(doc.GetText().Contains("{{ Column2 }}"), preserveUnusedTags);

    if (preserveUnusedTags)
        Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
    else
        Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
}

/// <summary>
/// Создайте документ и добавьте два тега открытого текста, которые могут действовать как поля MERGEFIELD во время слияния почты.
/// </summary>
private static Document CreateSourceDocWithAlternativeMergeFields()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("{{ Column1 }}");
    builder.Writeln("{{ Column2 }}");

    // Наши теги будут регистрироваться как места назначения для данных слияния почты, только если мы установим для этого параметра значение true.
    doc.MailMerge.UseNonMergeFields = true;

    return doc;
}

/// <summary>
/// Создайте простую таблицу данных с одним столбцом.
/// </summary>
private static DataTable CreateSourceTablePreserveUnusedTags()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("Column1");
    dataTable.Rows.Add(new object[] { "Value1" });

    return dataTable;
}
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../mailmerge/)
* сборка [Aspose.Words](../../../)


