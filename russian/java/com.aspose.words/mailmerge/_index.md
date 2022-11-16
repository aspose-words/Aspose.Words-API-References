---
title: MailMerge
second_title: Справочник по API Aspose.Words для Java
description: Представляет функцию слияния почты.
type: docs
weight: 379
url: /ru/java/com.aspose.words/mailmerge/
---

**Наследование:**
java.lang.Object
```
public class MailMerge
```

Представляет функцию слияния почты.

 Чтобы узнать больше, посетите**Mail Merge and Reporting** документальная статья.

Чтобы операция слияния работала, документ должен содержать поля Word MERGEFIELD и, возможно, NEXT. Во время операции слияния поля слияния в документе заменяются значениями из вашего источника данных.

Существует два разных способа использования слияния: с областями слияния и без них.

 Самое простое слияние без регионов и очень похоже на то, как работает слияние в Word. Используйте методы Execute для слияния информации из какого-либо источника данных, например**DataTable**, **DataSet** или массив объектов в ваш документ.**MailMerge**объект обрабатывает все записи источника данных, копирует и добавляет содержимое всего документа для каждой записи.

 Обратите внимание, что когда**MailMerge** объект встречает поле NEXT, он выбирает следующую запись в источнике данных и продолжает слияние без копирования какого-либо содержимого.

Используйте методы ExecuteWithRegions для объединения информации в документ с определенными областями слияния. Вы можете использовать или в качестве источников данных для этой операции.

Вам нужно использовать области слияния, если вы хотите динамически увеличивать части внутри документа. Без областей слияния весь документ будет повторяться для каждой записи источника данных.
## Методы

| Метод | Описание |
| --- | --- |
| [deleteFields()](#deleteFields--) | Удаляет поля, связанные со слиянием почты, из документа. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [execute(IMailMergeDataSource dataSource)](#execute-com.aspose.words.IMailMergeDataSource-) | Выполняет слияние почты из пользовательского источника данных. |
| [execute(System.Data.DataRow row)](#execute-com.aspose.words.net.System.Data.DataRow-) | Выполняет слияние почты из DataRow в документ. |
| [execute(System.Data.DataTable table)](#execute-com.aspose.words.net.System.Data.DataTable-) | Выполняет слияние почты из com.aspose.words.net.System.Data.DataTable в документ. |
| [execute(System.Data.DataView dataView)](#execute-com.aspose.words.net.System.Data.DataView-) | Выполняет слияние почты из DataView в документ. |
| [execute(System.Data.IDataReader dataReader)](#execute-com.aspose.words.net.System.Data.IDataReader-) | Выполняет слияние почты из IDataReader в документ. |
| [execute(String[] fieldNames, Object[] values)](#execute-java.lang.String---java.lang.Object---) | Выполняет операцию слияния почты. |
| [executeWithRegions(IMailMergeDataSource dataSource)](#executeWithRegions-com.aspose.words.IMailMergeDataSource-) | Выполняет слияние из пользовательского источника данных с областями слияния. |
| [executeWithRegions(IMailMergeDataSourceRoot dataSourceRoot)](#executeWithRegions-com.aspose.words.IMailMergeDataSourceRoot-) | Выполняет слияние из пользовательского источника данных с областями слияния. |
| [executeWithRegions(System.Data.DataSet dataSet)](#executeWithRegions-com.aspose.words.net.System.Data.DataSet-) | Выполняет операцию слияния в документ с областями слияния. |
| [executeWithRegions(System.Data.DataTable dataTable)](#executeWithRegions-com.aspose.words.net.System.Data.DataTable-) | Выполняет слияние почты из DataTable в документ с областями слияния. |
| [executeWithRegions(System.Data.DataView dataView)](#executeWithRegions-com.aspose.words.net.System.Data.DataView-) | Выполняет слияние почты из DataView в документ с областями слияния. |
| [executeWithRegions(System.Data.IDataReader dataReader, String tableName)](#executeWithRegions-com.aspose.words.net.System.Data.IDataReader-java.lang.String-) | Выполняет слияние почты из IDataReader в документ с областями слияния. |
| [getClass()](#getClass--) |  |
| [getCleanupOptions()](#getCleanupOptions--) | Получает набор флагов, указывающих, какие элементы следует удалить во время слияния. |
| [getCleanupParagraphsWithPunctuationMarks()](#getCleanupParagraphsWithPunctuationMarks--) |  Получает значение, указывающее, считаются ли абзацы со знаками препинания пустыми и должны ли они быть удалены, если[MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-EMPTY-PARAGRAPHS) опция указана. |
| [getFieldMergingCallback()](#getFieldMergingCallback--) | Происходит во время слияния, когда в документе встречается поле слияния. |
| [getFieldNames()](#getFieldNames--) | Возвращает коллекцию имен полей слияния, доступных в документе. |
| [getFieldNamesForRegion(String regionName)](#getFieldNamesForRegion-java.lang.String-) | Получить имена полей слияния из региона. |
| [getFieldNamesForRegion(String regionName, int regionIndex)](#getFieldNamesForRegion-java.lang.String-int-) | Возвращает коллекцию имен полей слияния, доступных в регионе. |
| [getMailMergeCallback()](#getMailMergeCallback--) | Позволяет обрабатывать определенные события во время слияния почты. |
| [getMappedDataFields()](#getMappedDataFields--) | Возвращает коллекцию, представляющую сопоставленные поля данных для операции слияния. |
| [getMergeDuplicateRegions()](#getMergeDuplicateRegions--) | Получает значение, указывающее, следует ли объединять все области слияния документов с именем источника данных при выполнении слияния с областями для источника данных или только первую. |
| [getMergeWholeDocument()](#getMergeWholeDocument--) | Получает значение, указывающее, обновляются ли поля во всем документе при выполнении слияния почты с областями. |
| [getPreserveUnusedTags()](#getPreserveUnusedTags--) | Получает значение, указывающее, следует ли сохранять неиспользуемые теги «усы». |
| [getRegionEndTag()](#getRegionEndTag--) | Получает конечный тег области слияния. |
| [getRegionStartTag()](#getRegionStartTag--) | Получает начальный тег области слияния. |
| [getRegionsByName(String regionName)](#getRegionsByName-java.lang.String-) | Возвращает коллекцию областей слияния с указанным именем. |
| [getRegionsHierarchy()](#getRegionsHierarchy--) | Возвращает полную иерархию областей (с полями), доступных в документе. |
| [getRestartListsAtEachSection()](#getRestartListsAtEachSection--) | Получает значение, указывающее, перезапускаются ли списки в каждом разделе после выполнения слияния. |
| [getRetainFirstSectionStart()](#getRetainFirstSectionStart--) | Получает значение, указывающее, является ли[PageSetup.getSectionStart()](../../com.aspose.words/pagesetup\#getSectionStart--) / [PageSetup.setSectionStart(int)](../../com.aspose.words/pagesetup\#setSectionStart-int-) первого раздела документа и его копии для последующих строк источника данных сохраняются во время слияния или обновляются в соответствии с поведением MS Word. |
| [getTrimWhitespaces()](#getTrimWhitespaces--) | Получает значение, указывающее, обрезаются ли конечные и начальные пробелы из значений слияния. |
| [getUnconditionalMergeFieldsAndRegions()](#getUnconditionalMergeFieldsAndRegions--) | Получает значение, указывающее, объединяются ли поля слияния и области слияния независимо от условия родительского поля ЕСЛИ. |
| [getUseNonMergeFields()](#getUseNonMergeFields--) | Значение true указывает, что в дополнение к полям MERGEFIELD слияние выполняется с некоторыми другими типами полей, а также с "\{\{имя поля\}\}" теги. |
| [getUseWholeParagraphAsRegion()](#getUseWholeParagraphAsRegion--) | Получает значение, указывающее, следует ли включать в область слияния весь абзац с полем TableStart или TableEnd или определенный диапазон между полями TableStart и TableEnd. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setCleanupOptions(int value)](#setCleanupOptions-int-) | Задает набор флагов, указывающих, какие элементы должны быть удалены во время слияния. |
| [setCleanupParagraphsWithPunctuationMarks(boolean value)](#setCleanupParagraphsWithPunctuationMarks-boolean-) |  Задает значение, указывающее, считаются ли абзацы со знаками препинания пустыми и должны ли они быть удалены, если[MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-EMPTY-PARAGRAPHS) опция указана. |
| [setFieldMergingCallback(IFieldMergingCallback value)](#setFieldMergingCallback-com.aspose.words.IFieldMergingCallback-) | Происходит во время слияния, когда в документе встречается поле слияния. |
| [setMailMergeCallback(IMailMergeCallback value)](#setMailMergeCallback-com.aspose.words.IMailMergeCallback-) | Позволяет обрабатывать определенные события во время слияния почты. |
| [setMergeDuplicateRegions(boolean value)](#setMergeDuplicateRegions-boolean-) | Задает значение, указывающее, должны ли объединяться все области слияния документов с именем источника данных при выполнении слияния с областями для источника данных или только первая. |
| [setMergeWholeDocument(boolean value)](#setMergeWholeDocument-boolean-) | Задает значение, указывающее, обновляются ли поля во всем документе при выполнении слияния почты с областями. |
| [setPreserveUnusedTags(boolean value)](#setPreserveUnusedTags-boolean-) | Устанавливает значение, указывающее, следует ли сохранять неиспользуемые теги «усы». |
| [setRegionEndTag(String value)](#setRegionEndTag-java.lang.String-) | Устанавливает конечный тег области слияния. |
| [setRegionStartTag(String value)](#setRegionStartTag-java.lang.String-) | Задает начальный тег области слияния. |
| [setRestartListsAtEachSection(boolean value)](#setRestartListsAtEachSection-boolean-) | Задает значение, указывающее, перезапускаются ли списки в каждом разделе после выполнения слияния. |
| [setRetainFirstSectionStart(boolean value)](#setRetainFirstSectionStart-boolean-) |  Устанавливает значение, указывающее,[PageSetup.getSectionStart()](../../com.aspose.words/pagesetup\#getSectionStart--) / [PageSetup.setSectionStart(int)](../../com.aspose.words/pagesetup\#setSectionStart-int-) первого раздела документа и его копии для последующих строк источника данных сохраняются во время слияния или обновляются в соответствии с поведением MS Word. |
| [setTrimWhitespaces(boolean value)](#setTrimWhitespaces-boolean-) | Задает значение, указывающее, обрезаются ли конечные и начальные пробелы из значений слияния. |
| [setUnconditionalMergeFieldsAndRegions(boolean value)](#setUnconditionalMergeFieldsAndRegions-boolean-) | Задает значение, указывающее, объединяются ли поля слияния и области слияния независимо от условия родительского поля ЕСЛИ. |
| [setUseNonMergeFields(boolean value)](#setUseNonMergeFields-boolean-) | Значение true указывает, что в дополнение к полям MERGEFIELD слияние выполняется с некоторыми другими типами полей, а также с "\{\{имя поля\}\}" теги. |
| [setUseWholeParagraphAsRegion(boolean value)](#setUseWholeParagraphAsRegion-boolean-) | Задает значение, указывающее, следует ли включать в область слияния весь абзац с полем TableStart или TableEnd или определенный диапазон между полями TableStart и TableEnd. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### deleteFields() {#deleteFields--}
```
public void deleteFields()
```


Удаляет поля, связанные со слиянием почты, из документа.

Этот метод удаляет поля MERGEFIELD и NEXT из документа.

Этот метод может быть полезен, если ваша операция слияния не всегда требует заполнения всех полей в документе. Используйте этот метод, чтобы удалить все оставшиеся поля слияния.

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Возвращает:**
логический
### execute(IMailMergeDataSource dataSource) {#execute-com.aspose.words.IMailMergeDataSource-}
```
public void execute(IMailMergeDataSource dataSource)
```


Выполняет слияние почты из пользовательского источника данных.

 Используйте этот метод для заполнения полей слияния в документе значениями из любого источника данных, например списка, хеш-таблицы или объектов. Вам нужно написать свой собственный класс, реализующий[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource) интерфейс.

 Вы можете использовать этот метод только тогда, когда[FieldOptions.isBidiTextSupportedOnUpdate()](../../com.aspose.words/fieldoptions\#isBidiTextSupportedOnUpdate--) / [FieldOptions.isBidiTextSupportedOnUpdate(boolean)](../../com.aspose.words/fieldoptions\#isBidiTextSupportedOnUpdate-boolean-) неверно, то есть вам не нужна совместимость с языками с письмом справа налево (такими как арабский или иврит).

 Этот метод игнорирует[MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-UNUSED-REGIONS) вариант.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataSource | [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource) | Объект, реализующий настраиваемый интерфейс источника данных для слияния почты. |

### execute(System.Data.DataRow row) {#execute-com.aspose.words.net.System.Data.DataRow-}
```
public void execute(System.Data.DataRow row)
```


Выполняет слияние почты из DataRow в документ.

 Используйте этот метод для заполнения полей слияния в документе значениями из**DataRow**.

 Этот метод игнорирует[MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-UNUSED-REGIONS) вариант.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow) | Строка, содержащая данные для вставки в поля слияния. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |

### execute(System.Data.DataTable table) {#execute-com.aspose.words.net.System.Data.DataTable-}
```
public void execute(System.Data.DataTable table)
```


Выполняет слияние почты из com.aspose.words.net.System.Data.DataTable в документ.

 Используйте этот метод для заполнения полей слияния в документе значениями из**DataTable**.

Все записи из таблицы объединяются в документ.

 Вы можете использовать поле NEXT в документе Word, чтобы вызвать**MailMerge** объект для выбора следующей записи из**DataTable** и продолжить слияние. Это можно использовать при создании таких документов, как почтовые этикетки.

 Когда**MailMerge** объект достигает конца основного документа, а в**DataTable**, он копирует все содержимое основного документа и добавляет его в конец целевого документа, используя в качестве разделителя разрыв раздела.

 Этот метод игнорирует[MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-UNUSED-REGIONS) вариант.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable) | Таблица, содержащая данные для вставки в поля слияния. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |

### execute(System.Data.DataView dataView) {#execute-com.aspose.words.net.System.Data.DataView-}
```
public void execute(System.Data.DataView dataView)
```


Выполняет слияние почты из DataView в документ.

 Этот метод полезен, если вы извлекаете данные в**DataTable** но затем необходимо применить фильтр или сортировку перед слиянием почты.

Обратите внимание, что этот метод не использует области слияния почты, и для нескольких записей документ будет увеличиваться за счет повторения всего документа.

 Этот метод игнорирует[MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-UNUSED-REGIONS) вариант.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataView | [DataView](../../com.aspose.words.net.system.data/dataview) | Источник данных для операции слияния почты. |

### execute(System.Data.IDataReader dataReader) {#execute-com.aspose.words.net.System.Data.IDataReader-}
```
public void execute(System.Data.IDataReader dataReader)
```


Выполняет слияние почты из IDataReader в документ.

 Вы можете пройти**SqlDataReader** или же**OleDbDataReader** объект в этот метод в качестве параметра, потому что они оба реализовали**IDataReader** интерфейс.

Обратите внимание, что этот метод не использует области слияния почты, и для нескольких записей документ будет увеличиваться за счет повторения всего документа.

 Этот метод игнорирует[MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-UNUSED-REGIONS) вариант.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataReader | [IDataReader](../../com.aspose.words.net.system.data/idatareader) | Источник данных для операции слияния почты. |

### execute(String[] fieldNames, Object[] values) {#execute-java.lang.String---java.lang.Object---}
```
public void execute(String[] fieldNames, Object[] values)
```


Выполняет операцию слияния почты. Выполняет операцию слияния почты для одной записи.

Используйте этот метод для заполнения полей слияния в документе значениями из массива объектов.

Этот метод объединяет данные только для одной записи. Массив имен полей и массив значений представляют собой данные одной записи.

Этот метод не использует регионы слияния.

 Этот метод игнорирует[MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-UNUSED-REGIONS) вариант.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldNames | java.lang.String[] | Массив имен полей слияния. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |
| values | java.lang.Object[] | Массив значений для вставки в поля слияния. Количество элементов в этом массиве должно совпадать с количеством элементов в fieldNames. |

### executeWithRegions(IMailMergeDataSource dataSource) {#executeWithRegions-com.aspose.words.IMailMergeDataSource-}
```
public void executeWithRegions(IMailMergeDataSource dataSource)
```


Выполняет слияние из пользовательского источника данных с областями слияния.

Используйте этот метод, чтобы заполнить поля слияния в документе значениями из любого пользовательского источника данных, такого как XML-файл или коллекции бизнес-объектов. Вам нужно написать свой собственный класс, реализующий[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource) интерфейс.

 Вы можете использовать этот метод только тогда, когда[FieldOptions.isBidiTextSupportedOnUpdate()](../../com.aspose.words/fieldoptions\#isBidiTextSupportedOnUpdate--) / [FieldOptions.isBidiTextSupportedOnUpdate(boolean)](../../com.aspose.words/fieldoptions\#isBidiTextSupportedOnUpdate-boolean-) неверно, то есть вам не нужна совместимость с языками с письмом справа налево (такими как арабский или иврит).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataSource | [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource) | Объект, реализующий настраиваемый интерфейс источника данных для слияния почты. |

### executeWithRegions(IMailMergeDataSourceRoot dataSourceRoot) {#executeWithRegions-com.aspose.words.IMailMergeDataSourceRoot-}
```
public void executeWithRegions(IMailMergeDataSourceRoot dataSourceRoot)
```


Выполняет слияние из пользовательского источника данных с областями слияния.

 Используйте этот метод, чтобы заполнить поля слияния в документе значениями из любого пользовательского источника данных, такого как XML-файл или коллекции бизнес-объектов. Вам нужно написать свои собственные классы, которые реализуют[IMailMergeDataSourceRoot](../../com.aspose.words/imailmergedatasourceroot) а также[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource) интерфейсы.

 Вы можете использовать этот метод только тогда, когда[FieldOptions.isBidiTextSupportedOnUpdate()](../../com.aspose.words/fieldoptions\#isBidiTextSupportedOnUpdate--) / [FieldOptions.isBidiTextSupportedOnUpdate(boolean)](../../com.aspose.words/fieldoptions\#isBidiTextSupportedOnUpdate-boolean-) неверно, то есть вам не нужна совместимость с языками с письмом справа налево (такими как арабский или иврит).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataSourceRoot | [IMailMergeDataSourceRoot](../../com.aspose.words/imailmergedatasourceroot) | Объект, реализующий настраиваемый корневой интерфейс источника данных слияния. |

### executeWithRegions(System.Data.DataSet dataSet) {#executeWithRegions-com.aspose.words.net.System.Data.DataSet-}
```
public void executeWithRegions(System.Data.DataSet dataSet)
```


Выполняет операцию слияния в документ с областями слияния. Поддерживает источники данных «родитель-потомок» (основной-подробности) и вложенные области слияния почты. Выполняет слияние почты из набора данных в документ с областями слияния.

Используйте этот метод для выполнения слияния из одной или нескольких таблиц в повторяющиеся области слияния в документе. Области слияния внутри документа будут динамически увеличиваться, чтобы вместить записи в соответствующих таблицах.

В документе должны быть определены области слияния с именами, которые ссылаются на таблицы в наборе данных.

Чтобы указать область слияния в документе, вам нужно вставить два поля слияния, чтобы отметить начало и конец области слияния.

Все содержимое документа, включенного в область слияния, будет автоматически повторяться для каждой записи в DataTable.

Чтобы отметить начало области слияния, вставьте MERGEFIELD с именем TableStart:MyTable, где MyTable соответствует одному из имен таблиц в вашем наборе данных.

Чтобы отметить конец области слияния, вставьте еще одно поле MERGEFIELD с именем TableEnd:MyTable.

Чтобы вставить MERGEFIELD в Word, используйте команду Insert/Field и выберите MergeField, затем введите имя поля.

Поля TableStart и TableEnd должны находиться в одном и том же разделе документа.

При использовании внутри таблицы TableStart и TableEnd должны находиться в одной и той же строке таблицы.

Области слияния в документе должны быть правильно сформированы (всегда должна быть пара совпадающих полей слияния TableStart и TableEnd с одинаковым именем таблицы).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset) | Набор данных, содержащий данные для вставки в поля слияния. |

### executeWithRegions(System.Data.DataTable dataTable) {#executeWithRegions-com.aspose.words.net.System.Data.DataTable-}
```
public void executeWithRegions(System.Data.DataTable dataTable)
```


Выполняет слияние почты из DataTable в документ с областями слияния.

Если в документе определены другие области слияния, они остаются нетронутыми. Это позволяет выполнять несколько операций слияния почты.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable) |  Источник данных для операции слияния почты. Таблица должна иметь свой**TableName** набор свойств. |

### executeWithRegions(System.Data.DataView dataView) {#executeWithRegions-com.aspose.words.net.System.Data.DataView-}
```
public void executeWithRegions(System.Data.DataView dataView)
```


Выполняет слияние почты из DataView в документ с областями слияния.

 Этот метод полезен, если вы извлекаете данные в**DataTable** но затем необходимо применить фильтр или сортировку перед слиянием почты.

 В документе должна быть определена область слияния с именем, совпадающим**DataView.Table.TableName**.

Если в документе определены другие области слияния, они остаются нетронутыми. Это позволяет выполнять несколько операций слияния почты.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataView | [DataView](../../com.aspose.words.net.system.data/dataview) |  Источник данных для операции слияния почты. Исходная таблица**DataView** должен иметь свой**TableName** набор свойств. |

### executeWithRegions(System.Data.IDataReader dataReader, String tableName) {#executeWithRegions-com.aspose.words.net.System.Data.IDataReader-java.lang.String-}
```
public void executeWithRegions(System.Data.IDataReader dataReader, String tableName)
```


Выполняет слияние почты из IDataReader в документ с областями слияния.

 Вы можете пройти**SqlDataReader** или же**OleDbDataReader** объект в этот метод в качестве параметра, потому что они оба реализовали**IDataReader** интерфейс.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataReader | [IDataReader](../../com.aspose.words.net.system.data/idatareader) | Источник записей данных для слияния, например OleDbDataReader или SqlDataReader. |
| tableName | java.lang.String | Имя области слияния в документе для заполнения. |

### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getCleanupOptions() {#getCleanupOptions--}
```
public int getCleanupOptions()
```


Получает набор флагов, указывающих, какие элементы следует удалить во время слияния.

**Возвращает:**
 int — набор флагов, указывающих, какие элементы следует удалить во время слияния. Возвращаемое значение представляет собой побитовую комбинацию[MailMergeCleanupOptions](../../com.aspose.words/mailmergecleanupoptions) константы.
### getCleanupParagraphsWithPunctuationMarks() {#getCleanupParagraphsWithPunctuationMarks--}
```
public boolean getCleanupParagraphsWithPunctuationMarks()
```


 Получает значение, указывающее, считаются ли абзацы со знаками препинания пустыми и должны ли они быть удалены, если[MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-EMPTY-PARAGRAPHS)опция указана. Значение по умолчанию верно . Вот полный список очищаемых знаков препинания:

 *  !
 *  ,
 *  .
 *  :
 *  ;
 *  ?
 *  �
 *  �

**Возвращает:**
 логическое значение — значение, указывающее, считаются ли абзацы со знаками препинания пустыми и должны ли они быть удалены, если[MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-EMPTY-PARAGRAPHS) опция указана.
### getFieldMergingCallback() {#getFieldMergingCallback--}
```
public IFieldMergingCallback getFieldMergingCallback()
```


Происходит во время слияния, когда в документе встречается поле слияния.

**Возвращает:**
[IFieldMergingCallback](../../com.aspose.words/ifieldmergingcallback) - соответствующий[IFieldMergingCallback](../../com.aspose.words/ifieldmergingcallback) ценность.
### getFieldNames() {#getFieldNames--}
```
public String[] getFieldNames()
```


Возвращает коллекцию имен полей слияния, доступных в документе.

Возвращает полные имена полей слияния, включая необязательный префикс. Не устраняет повторяющиеся имена полей.

Новая строка[] создается при каждом вызове.

 Включает имена полей «усы», если[getUseNonMergeFields()](../../com.aspose.words/mailmerge\#getUseNonMergeFields--) / [setUseNonMergeFields(boolean)](../../com.aspose.words/mailmerge\#setUseNonMergeFields-boolean-) является**true**.

**Возвращает:**
java.lang.String[]
### getFieldNamesForRegion(String regionName) {#getFieldNamesForRegion-java.lang.String-}
```
public String[] getFieldNamesForRegion(String regionName)
```


Получить имена полей слияния из региона. Возвращает коллекцию имен полей слияния, доступных в регионе.

Возвращает полные имена полей слияния, включая необязательный префикс. Не устраняет повторяющиеся имена полей.

Если документ содержит несколько регионов с одинаковым названием, обрабатывается самый первый регион.

Новый массив строк создается при каждом вызове.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| regionName | java.lang.String | Название региона (без учета регистра). |

**Возвращает:**
java.lang.String[]
### getFieldNamesForRegion(String regionName, int regionIndex) {#getFieldNamesForRegion-java.lang.String-int-}
```
public String[] getFieldNamesForRegion(String regionName, int regionIndex)
```


Возвращает коллекцию имен полей слияния, доступных в регионе.

Возвращает полные имена полей слияния, включая необязательный префикс. Не устраняет повторяющиеся имена полей.

Если документ содержит несколько регионов с одинаковыми именами, обрабатывается N-й регион (начиная с нуля).

Новый массив строк создается при каждом вызове.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| regionName | java.lang.String | Название региона (без учета регистра). |
| regionIndex | int | Индекс региона (с нуля). |

**Возвращает:**
java.lang.String[]
### getMailMergeCallback() {#getMailMergeCallback--}
```
public IMailMergeCallback getMailMergeCallback()
```


Позволяет обрабатывать определенные события во время слияния почты.

**Возвращает:**
[IMailMergeCallback](../../com.aspose.words/imailmergecallback) - соответствующий[IMailMergeCallback](../../com.aspose.words/imailmergecallback) ценность.
### getMappedDataFields() {#getMappedDataFields--}
```
public MappedDataFieldCollection getMappedDataFields()
```


Возвращает коллекцию, представляющую сопоставленные поля данных для операции слияния.

Сопоставленные поля данных позволяют автоматически сопоставлять имена полей в источнике данных и имена полей слияния в документе.

**Возвращает:**
[MappedDataFieldCollection](../../com.aspose.words/mappeddatafieldcollection) — Коллекция, представляющая сопоставленные поля данных для операции слияния почты.
### getMergeDuplicateRegions() {#getMergeDuplicateRegions--}
```
public boolean getMergeDuplicateRegions()
```


 Получает значение, указывающее, следует ли объединять все области слияния документов с именем источника данных при выполнении слияния с областями для источника данных или только первую. Значение по умолчанию**false**.

**Возвращает:**
логическое значение — значение, указывающее, должны ли объединяться все области слияния документов с именем источника данных при выполнении слияния с областями для источника данных или только первая.
### getMergeWholeDocument() {#getMergeWholeDocument--}
```
public boolean getMergeWholeDocument()
```


 Получает значение, указывающее, обновляются ли поля во всем документе при выполнении слияния почты с областями. Значение по умолчанию**false**.

**Возвращает:**
логическое значение — значение, указывающее, обновляются ли поля во всем документе при выполнении слияния почты с областями.
### getPreserveUnusedTags() {#getPreserveUnusedTags--}
```
public boolean getPreserveUnusedTags()
```


Получает значение, указывающее, следует ли сохранять неиспользуемые теги «усы». Значение по умолчанию**false**.

**Возвращает:**
boolean — значение, указывающее, следует ли сохранять неиспользуемые теги «усы».
### getRegionEndTag() {#getRegionEndTag--}
```
public String getRegionEndTag()
```


Получает конечный тег области слияния.

**Возвращает:**
java.lang.String — конечный тег области слияния.
### getRegionStartTag() {#getRegionStartTag--}
```
public String getRegionStartTag()
```


Получает начальный тег области слияния.

**Возвращает:**
java.lang.String — начальный тег области слияния.
### getRegionsByName(String regionName) {#getRegionsByName-java.lang.String-}
```
public ArrayList getRegionsByName(String regionName)
```


Возвращает коллекцию областей слияния с указанным именем.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| regionName | java.lang.String | Название региона (без учета регистра). |

**Возвращает:**
java.util.ArrayList — Список регионов.
### getRegionsHierarchy() {#getRegionsHierarchy--}
```
public MailMergeRegionInfo getRegionsHierarchy()
```


Возвращает полную иерархию областей (с полями), доступных в документе.

 Иерархия возвращается в виде[MailMergeRegionInfo](../../com.aspose.words/mailmergeregioninfo) учебный класс.

**Возвращает:**
[MailMergeRegionInfo](../../com.aspose.words/mailmergeregioninfo) - Иерархия регионов.
### getRestartListsAtEachSection() {#getRestartListsAtEachSection--}
```
public boolean getRestartListsAtEachSection()
```


 Получает значение, указывающее, перезапускаются ли списки в каждом разделе после выполнения слияния. Значение по умолчанию**true**.

**Возвращает:**
логическое значение — значение, указывающее, перезапускаются ли списки в каждом разделе после выполнения слияния.
### getRetainFirstSectionStart() {#getRetainFirstSectionStart--}
```
public boolean getRetainFirstSectionStart()
```


Получает значение, указывающее, является ли[PageSetup.getSectionStart()](../../com.aspose.words/pagesetup\#getSectionStart--) / [PageSetup.setSectionStart(int)](../../com.aspose.words/pagesetup\#setSectionStart-int-) первого раздела документа и его копии для последующих строк источника данных сохраняются во время слияния или обновляются в соответствии с поведением MS Word. Значение по умолчанию**true**.

**Возвращает:**
 boolean - значение, указывающее, является ли[PageSetup.getSectionStart()](../../com.aspose.words/pagesetup\#getSectionStart--) / [PageSetup.setSectionStart(int)](../../com.aspose.words/pagesetup\#setSectionStart-int-) первого раздела документа и его копии для последующих строк источника данных сохраняются во время слияния или обновляются в соответствии с поведением MS Word.
### getTrimWhitespaces() {#getTrimWhitespaces--}
```
public boolean getTrimWhitespaces()
```


Получает значение, указывающее, обрезаются ли конечные и начальные пробелы из значений слияния. Значение по умолчанию**true**.

**Возвращает:**
boolean — значение, указывающее, обрезаются ли конечные и ведущие пробелы из значений слияния почты.
### getUnconditionalMergeFieldsAndRegions() {#getUnconditionalMergeFieldsAndRegions--}
```
public boolean getUnconditionalMergeFieldsAndRegions()
```


 Получает значение, указывающее, объединяются ли поля слияния и области слияния независимо от условия родительского поля ЕСЛИ. Значение по умолчанию**false**.

**Возвращает:**
логическое значение — значение, указывающее, объединяются ли поля слияния и области слияния независимо от условия родительского поля IF.
### getUseNonMergeFields() {#getUseNonMergeFields--}
```
public boolean getUseNonMergeFields()
```


Значение true указывает, что в дополнение к полям MERGEFIELD слияние выполняется с некоторыми другими типами полей, а также с "\{\{имя поля\}\}" теги.

Обычно слияние почты выполняется только в полях MERGEFIELD, но несколько клиентов построили свои отчеты с использованием других полей и таким образом создали множество документов. Для упрощения миграции (и поскольку этот подход использовался несколькими клиентами независимо друг от друга) была введена возможность слияния почты с другими полями.

 Когда**UseNonMergeFields** установлено значение true, Aspose.Words будет выполнять слияние почты в следующие поля:

MERGEFIELD имя поля

MACROBUTTON NOMACRO Имя поля

ЕСЛИ 0 = 0 "\{имя поля\}" ""

 Кроме того, когда**UserNonMergeFields** установлено значение true, Aspose.Words будет выполнять слияние почты в текстовые теги "\{\{имя поля\}\}". Это не поля, а просто текстовые теги.

**Возвращает:**
boolean - соответствующее логическое значение.
### getUseWholeParagraphAsRegion() {#getUseWholeParagraphAsRegion--}
```
public boolean getUseWholeParagraphAsRegion()
```


 Получает значение, указывающее, следует ли включать в область слияния весь абзац с полем TableStart или TableEnd или определенный диапазон между полями TableStart и TableEnd. Значение по умолчанию**true**.

**Возвращает:**
boolean — значение, указывающее, следует ли включать в область слияния весь абзац с полем TableStart или TableEnd или определенный диапазон между полями TableStart и TableEnd.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setCleanupOptions(int value) {#setCleanupOptions-int-}
```
public void setCleanupOptions(int value)
```


Задает набор флагов, указывающих, какие элементы должны быть удалены во время слияния.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Набор флагов, указывающих, какие элементы должны быть удалены во время слияния. Значение должно быть побитовой комбинацией[MailMergeCleanupOptions](../../com.aspose.words/mailmergecleanupoptions) константы. |

### setCleanupParagraphsWithPunctuationMarks(boolean value) {#setCleanupParagraphsWithPunctuationMarks-boolean-}
```
public void setCleanupParagraphsWithPunctuationMarks(boolean value)
```


 Задает значение, указывающее, считаются ли абзацы со знаками препинания пустыми и должны ли они быть удалены, если[MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-EMPTY-PARAGRAPHS)опция указана. Значение по умолчанию верно . Вот полный список очищаемых знаков препинания:

 *  !
 *  ,
 *  .
 *  :
 *  ;
 *  ?
 *  �
 *  �

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  Значение, указывающее, считаются ли абзацы со знаками препинания пустыми и должны ли они быть удалены, если[MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-EMPTY-PARAGRAPHS) опция указана. |

### setFieldMergingCallback(IFieldMergingCallback value) {#setFieldMergingCallback-com.aspose.words.IFieldMergingCallback-}
```
public void setFieldMergingCallback(IFieldMergingCallback value)
```


Происходит во время слияния, когда в документе встречается поле слияния.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IFieldMergingCallback](../../com.aspose.words/ifieldmergingcallback) |  Соответствующий[IFieldMergingCallback](../../com.aspose.words/ifieldmergingcallback) ценность. |

### setMailMergeCallback(IMailMergeCallback value) {#setMailMergeCallback-com.aspose.words.IMailMergeCallback-}
```
public void setMailMergeCallback(IMailMergeCallback value)
```


Позволяет обрабатывать определенные события во время слияния почты.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IMailMergeCallback](../../com.aspose.words/imailmergecallback) |  Соответствующий[IMailMergeCallback](../../com.aspose.words/imailmergecallback) ценность. |

### setMergeDuplicateRegions(boolean value) {#setMergeDuplicateRegions-boolean-}
```
public void setMergeDuplicateRegions(boolean value)
```


Задает значение, указывающее, должны ли объединяться все области слияния документов с именем источника данных при выполнении слияния с областями для источника данных или только первая. Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, указывающее, следует ли объединять все регионы слияния документов с именем источника данных при выполнении слияния с регионами для источника данных или только первый. |

### setMergeWholeDocument(boolean value) {#setMergeWholeDocument-boolean-}
```
public void setMergeWholeDocument(boolean value)
```


 Задает значение, указывающее, обновляются ли поля во всем документе при выполнении слияния почты с областями. Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, указывающее, обновляются ли поля во всем документе при выполнении слияния почты с областями. |

### setPreserveUnusedTags(boolean value) {#setPreserveUnusedTags-boolean-}
```
public void setPreserveUnusedTags(boolean value)
```


 Устанавливает значение, указывающее, следует ли сохранять неиспользуемые теги «усы». Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, указывающее, следует ли сохранять неиспользуемые теги «усы». |

### setRegionEndTag(String value) {#setRegionEndTag-java.lang.String-}
```
public void setRegionEndTag(String value)
```


Устанавливает конечный тег области слияния.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Конечный тег области слияния. |

### setRegionStartTag(String value) {#setRegionStartTag-java.lang.String-}
```
public void setRegionStartTag(String value)
```


Задает начальный тег области слияния.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Начальный тег области слияния. |

### setRestartListsAtEachSection(boolean value) {#setRestartListsAtEachSection-boolean-}
```
public void setRestartListsAtEachSection(boolean value)
```


Задает значение, указывающее, перезапускаются ли списки в каждом разделе после выполнения слияния. Значение по умолчанию**true**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, указывающее, перезапускаются ли списки в каждом разделе после выполнения слияния. |

### setRetainFirstSectionStart(boolean value) {#setRetainFirstSectionStart-boolean-}
```
public void setRetainFirstSectionStart(boolean value)
```


 Устанавливает значение, указывающее,[PageSetup.getSectionStart()](../../com.aspose.words/pagesetup\#getSectionStart--) / [PageSetup.setSectionStart(int)](../../com.aspose.words/pagesetup\#setSectionStart-int-) первого раздела документа и его копии для последующих строк источника данных сохраняются во время слияния или обновляются в соответствии с поведением MS Word. Значение по умолчанию**true**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  Значение, указывающее, является ли[PageSetup.getSectionStart()](../../com.aspose.words/pagesetup\#getSectionStart--) / [PageSetup.setSectionStart(int)](../../com.aspose.words/pagesetup\#setSectionStart-int-) первого раздела документа и его копии для последующих строк источника данных сохраняются во время слияния или обновляются в соответствии с поведением MS Word. |

### setTrimWhitespaces(boolean value) {#setTrimWhitespaces-boolean-}
```
public void setTrimWhitespaces(boolean value)
```


 Задает значение, указывающее, обрезаются ли конечные и начальные пробелы из значений слияния. Значение по умолчанию**true**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, указывающее, обрезаются ли конечные и начальные пробелы из значений слияния. |

### setUnconditionalMergeFieldsAndRegions(boolean value) {#setUnconditionalMergeFieldsAndRegions-boolean-}
```
public void setUnconditionalMergeFieldsAndRegions(boolean value)
```


 Задает значение, указывающее, объединяются ли поля слияния и области слияния независимо от условия родительского поля ЕСЛИ. Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, указывающее, объединяются ли поля слияния и области слияния независимо от условия родительского поля IF. |

### setUseNonMergeFields(boolean value) {#setUseNonMergeFields-boolean-}
```
public void setUseNonMergeFields(boolean value)
```


Значение true указывает, что в дополнение к полям MERGEFIELD слияние выполняется с некоторыми другими типами полей, а также с "\{\{имя поля\}\}" теги.

Обычно слияние почты выполняется только в полях MERGEFIELD, но несколько клиентов построили свои отчеты с использованием других полей и таким образом создали множество документов. Для упрощения миграции (и поскольку этот подход использовался несколькими клиентами независимо друг от друга) была введена возможность слияния почты с другими полями.

 Когда**UseNonMergeFields** установлено значение true, Aspose.Words будет выполнять слияние почты в следующие поля:

MERGEFIELD имя поля

MACROBUTTON NOMACRO Имя поля

ЕСЛИ 0 = 0 "\{имя поля\}" ""

 Кроме того, когда**UserNonMergeFields** установлено значение true, Aspose.Words будет выполнять слияние почты в текстовые теги "\{\{имя поля\}\}". Это не поля, а просто текстовые теги.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setUseWholeParagraphAsRegion(boolean value) {#setUseWholeParagraphAsRegion-boolean-}
```
public void setUseWholeParagraphAsRegion(boolean value)
```


 Задает значение, указывающее, следует ли включать в область слияния весь абзац с полем TableStart или TableEnd или определенный диапазон между полями TableStart и TableEnd. Значение по умолчанию**true**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, указывающее, следует ли включать в область слияния весь абзац с полем TableStart или TableEnd или определенный диапазон между полями TableStart и TableEnd. |

### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
