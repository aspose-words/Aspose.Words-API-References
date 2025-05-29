---
title: MailMerge Class
linktitle: MailMerge
articleTitle: MailMerge
second_title: Aspose.Words для .NET
description: Откройте мощные возможности слияния почты с классом Aspose.Words.MailMerging.MailMerge. Оптимизируйте создание документов и повысьте производительность без усилий!
type: docs
weight: 4530
url: /ru/net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

Представляет функциональность слияния почты.

Чтобы узнать больше, посетите[Слияние писем и отчетность](https://docs.aspose.com/words/net/mail-merge-and-reporting/) документальная статья.

```csharp
public class MailMerge
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions/) { get; set; } | Возвращает или задает набор флагов, которые определяют, какие элементы следует удалить во время слияния почты. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/) { get; set; } | Возвращает или задает значение, указывающее, считаются ли абзацы со знаками препинания пустыми и должны ли они быть удалены, еслиRemoveEmptyParagraphs опция указана. |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback/) { get; set; } | Возникает во время слияния почты, когда в документе встречается поле слияния почты. |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback/) { get; set; } | Позволяет обрабатывать определенные события во время слияния почты. |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields/) { get; } | Возвращает коллекцию, которая представляет сопоставленные поля данных для операции слияния почты. |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions/) { get; set; } | Возвращает или задает значение, указывающее, следует ли объединять все регионы слияния почты документа с именем источника данных при выполнении слияния почты с регионами по отношению к источнику данных или только первый из них. |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument/) { get; set; } | Возвращает или задает значение, указывающее, обновляются ли поля во всем документе при выполнении слияния почты с регионами. |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags/) { get; set; } | Возвращает или задает значение, указывающее, следует ли сохранять неиспользуемые теги «усы». |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag/) { get; set; } | Получает или задает конечный тег области слияния почты. |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag/) { get; set; } | Получает или задает начальный тег области слияния почты. |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection/) { get; set; } | Возвращает или задает значение, указывающее, перезапускаются ли списки в каждом разделе после выполнения слияния почты. |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart/) { get; set; } | Возвращает или задает значение, указывающее, является ли[`SectionStart`](../../aspose.words/pagesetup/sectionstart/) первого раздела документа и его копии для последующих строк источника данных сохраняются во время слияния почты или обновляются в соответствии с поведением MS Word. |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces/) { get; set; } | Возвращает или задает значение, указывающее, удаляются ли конечные и начальные пробелы из значений слияния почты. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/) { get; set; } | Возвращает или задает значение, указывающее, объединяются ли поля слияния и регионы слияния независимо от условия родительского поля IF. |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields/) { get; set; } | Когда`истинный` , указывает, что в дополнение к полям MERGEFIELD слияние выполняется в некоторые другие типы полей и также в теги "{{fieldName}}". |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/) { get; set; } | Возвращает или задает значение, указывающее, является ли весь абзац**TableStart** или**TableEnd** field или определенный диапазон между**TableStart** и**TableEnd** поля должны быть включены в область слияния почты. |

## Методы

| Имя | Описание |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields/)() | Удаляет из документа поля, связанные со слиянием. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_1)(*DataRow*) | Выполняет слияние почты из**DataRow** в документ. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_2)(*DataTable*) | Выполняет слияние почты из DataTable в документ. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_3)(*DataView*) | Выполняет слияние почты из**Просмотр данных** в документ. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_4)(*IDataReader*) | Выполняет слияние почты из**IDataReader** в документ. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute)(*[IMailMergeDataSource](../imailmergedatasource/)*) | Выполняет слияние почты из пользовательского источника данных. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_5)(*string[], object[]*) | Выполняет операцию слияния почты для одной записи. |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado/)(*object*) | Выполняет слияние почты из объекта ADO Recordset в документ. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_2)(*DataSet*) | Выполняет слияние почты из**Набор данных** в документ с областями слияния почты. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_3)(*DataTable*) | Выполняет слияние почты из**Таблица данных** в документ с областями слияния почты. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_4)(*DataView*) | Выполняет слияние почты из**Просмотр данных** в документ с областями слияния почты. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions)(*[IMailMergeDataSource](../imailmergedatasource/)*) | Выполняет слияние почты из пользовательского источника данных с областями слияния почты. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_1)(*[IMailMergeDataSourceRoot](../imailmergedatasourceroot/)*) | Выполняет слияние почты из пользовательского источника данных с областями слияния почты. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_5)(*IDataReader, string*) | Выполняет слияние почты из**IDataReader** в документ с областями слияния почты. |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado/)(*object, string*) | Выполняет слияние почты из объекта ADO Recordset в документ с областями слияния почты. |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames/)() | Возвращает коллекцию имен полей слияния, доступных в документе. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion)(*string*) | Возвращает коллекцию имен полей слияния, доступных в регионе. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion_1)(*string, int*) | Возвращает коллекцию имен полей слияния, доступных в регионе. |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname/)(*string*) | Возвращает коллекцию регионов слияния с указанным именем. |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy/)() | Возвращает полную иерархию регионов (с полями), доступных в документе. |

## Примечания

Для работы операции слияния почты документ должен содержать поля Word MERGEFIELD и опционально NEXT. Во время операции слияния почты поля слияния в документе заменяются значениями из вашего источника данных.

Существует два различных способа использования слияния почты: с областями слияния почты и без них.

Простейшее слияние почты выполняется без областей и очень похоже на то, как работает слияние почты в Word. ИспользуйтеВыполнять методы объединения информации из некоторого источника данных, например**Таблица данных** ,**Набор данных** ,**Просмотр данных** ,**IDataReader** или массив объектов в ваш документ. The `MailMerge` объект обрабатывает все записи источника данных и копирует и добавляет содержимое всего документа для каждой записи.

Обратите внимание, что когда`MailMerge`объект встречает поле NEXT, он выбирает следующую запись record в источнике данных и продолжает слияние, не копируя какое-либо содержимое.

Использовать[`ExecuteWithRegions`](./executewithregions/) и другие перегрузки для объединения информации в документ a с определенными областями слияния почты. Вы можете использовать **Набор данных** ,**Таблица данных** ,**Просмотр данных** или**IDataReader** в качестве источников данных для этой операции.

Вам необходимо использовать области слияния почты, если вы хотите динамически увеличивать части внутри документа . Без областей слияния почты весь документ будет повторяться для каждой записи источника данных.

## Примеры

Показывает, как выполнить слияние почты с данными из DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Ниже приведены два способа использования DataTable в качестве источника данных для слияния почты.
    // 1 - Использовать всю таблицу для слияния почты, чтобы создать один выходной документ слияния почты для каждой строки в таблице:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Используйте одну строку таблицы для создания одного выходного документа слияния:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Создает исходный документ для слияния почты.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Смотрите также

* пространство имен [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../)
