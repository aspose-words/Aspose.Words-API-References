---
title: MailMerge.PreserveUnusedTags
linktitle: PreserveUnusedTags
articleTitle: PreserveUnusedTags
second_title: Aspose.Words для .NET
description: MailMerge PreserveUnusedTags свойство. Получает или задает значение указывающее следует ли сохранять неиспользуемые теги усы на С#.
type: docs
weight: 80
url: /ru/net/aspose.words.mailmerging/mailmerge/preserveunusedtags/
---
## MailMerge.PreserveUnusedTags property

Получает или задает значение, указывающее, следует ли сохранять неиспользуемые теги «усы».

```csharp
public bool PreserveUnusedTags { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ` .

## Примеры

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

* property [UseNonMergeFields](../usenonmergefields/)
* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
