---
title: MailMerge
second_title: Справочник по API Aspose.Words для .NET
description: Представляет функцию слияния почты.
type: docs
weight: 3570
url: /ru/net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

Представляет функцию слияния почты.

```csharp
public class MailMerge
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions) { get; set; } | Получает или задает набор флагов, указывающих, какие элементы должны быть удалены при слиянии почты. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks) { get; set; } | Получает или задает значение, указывающее, считаются ли абзацы со знаками препинания пустыми и должны ли они быть удалены, еслиRemoveEmptyParagraphsуказана. |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback) { get; set; } | Происходит во время слияния, когда в документе встречается поле слияния. |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback) { get; set; } | Позволяет обрабатывать определенные события во время слияния почты. |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields) { get; } | Возвращает коллекцию, представляющую сопоставленные поля данных для операции слияния. |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions) { get; set; } | Получает или задает значение, указывающее, следует ли объединять все области слияния документов с именем источника данных при выполнении слияние почты с регионами против источника данных или только первого. |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument) { get; set; } | Получает или задает значение, указывающее, обновляются ли поля во всем документе при выполнении слияния почты с областями. |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags) { get; set; } | Получает или задает значение, указывающее, следует ли сохранять неиспользуемые теги "усы". |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag) { get; set; } | Получает или задает конечный тег области слияния. |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag) { get; set; } | Получает или задает начальный тег области слияния. |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection) { get; set; } | Получает или задает значение, указывающее, перезапускаются ли списки в каждом разделе после выполнения слияния. |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart) { get; set; } | Получает или задает значение, указывающее, будет ли[`SectionStart`](../../aspose.words/pagesetup/sectionstart)первого раздела документа и его копий для последующих строки источника данных сохраняются во время слияния или обновляются в соответствии с поведением MS Word. |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces) { get; set; } | Получает или задает значение, указывающее, удаляются ли конечные и начальные пробелы из значений слияния. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions) { get; set; } | Получает или задает значение, указывающее, объединяются ли поля слияния и области слияния независимо от условия родительского поля IF. |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields) { get; set; } | При значении true указывает, что в дополнение к полям MERGEFIELD слияние выполняется с некоторыми другими типами полей и также с "{{fieldName }}" теги. |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion) { get; set; } | Получает или задает значение, указывающее, следует ли включать в слияние весь абзац с полем TableStart или TableEnd или определенный диапазон между полями TableStart и TableEnd. область, край. |

## Методы

| Имя | Описание |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields)() | Удаляет из документа поля, связанные со слиянием. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute#execute_1)(DataRow) | Выполняет слияние почты из DataRow в документ. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute#execute_2)(DataTable) | Выполняет слияние почты из DataTable в документ. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute#execute_3)(DataView) | Выполняет слияние почты из DataView в документ. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute#execute_4)(IDataReader) | Выполняет слияние почты из IDataReader в документ. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute#execute)(IMailMergeDataSource) | Выполняет слияние почты из пользовательского источника данных. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute#execute_5)(string[], object[]) | Выполняет операцию слияния почты для одной записи. |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado)(object) | Выполняет слияние почты из объекта набора записей ADO в документ. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions#executewithregions_2)(DataSet) | Выполняет слияние почты из набора данных в документ с областями слияния. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions#executewithregions_3)(DataTable) | Выполняет слияние почты из DataTable в документ с областями слияния. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions#executewithregions_4)(DataView) | Выполняет слияние почты из DataView в документ с областями слияния. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions#executewithregions)(IMailMergeDataSource) | Выполняет слияние из пользовательского источника данных с областями слияния. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions#executewithregions_1)(IMailMergeDataSourceRoot) | Выполняет слияние из пользовательского источника данных с областями слияния. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions#executewithregions_5)(IDataReader, string) | Выполняет слияние почты из IDataReader в документ с областями слияния. |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado)(object, string) | Выполняет слияние почты из объекта набора записей ADO в документ с областями слияния. |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames)() | Возвращает коллекцию имен полей слияния, доступных в документе. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion#getfieldnamesforregion)(string) | Возвращает коллекцию имен полей слияния, доступных в регионе. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion#getfieldnamesforregion_1)(string, int) | Возвращает коллекцию имен полей слияния, доступных в регионе. |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname)(string) | Возвращает набор регионов слияния с указанным именем. |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy)() | Возвращает полную иерархию областей (с полями), доступных в документе. |

### Примечания

Для работы операции слияния документ должен содержать Word MERGEFIELD и необязательные поля NEXT. Во время операции слияния поля слияния в документе заменяются значениями из вашего источника данных.

Существует два разных способа использования слияния:с областями слияния и без них.

Простейшее слияние без регионов и очень похоже на то, как слияние почты работает в Word. Используйте методы Execute для объединения информации из некоторых источников данных, таких как **DataTable** , **DataSet** , **DataView** , **IDataReader** или массив объектов в ваш документ. Объект  **MailMerge** обрабатывает все записи источника данных, копирует и добавляет содержимое всего документа для каждая запись.

Обратите внимание, что когда объект **MailMerge** встречает поле NEXT, он выбирает следующую запись в источнике данных и продолжает слияние без копирования содержимого.

Используйте методы ExecuteWithRegions для объединения информации в документ с почтой определены области слияния. Вы можете использовать  **DataSet** , **DataTable** , **DataView** или **IDataReader** в качестве источников данных для этой операции.

Вам необходимо использовать области слияния почты, если вы хотите динамически увеличивать части внутри документа . Без областей слияния весь документ будет повторяться для каждой записи источника данных.

### Примеры

Показывает, как выполнить слияние почты с данными из DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

     // Ниже приведены два способа использования DataTable в качестве источника данных для слияния.
    // 1 — использовать всю таблицу для слияния, чтобы создать один выходной документ слияния для каждой строки в таблице: 
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

     // 2 - Используйте одну строку таблицы для создания одного выходного документа слияния почты: 
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
 /// Создает исходный документ слияния.
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

* namespace [Aspose.Words.MailMerging](../../aspose.words.mailmerging)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
