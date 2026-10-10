---
title: "ReportingEngine"
linktitle: "ReportingEngine"
second_title: "Aspose.Words для Java"
description: "Предоставляет процедуры для заполнения шаблонных документов данными и набор параметров для управления этими процедурами в Java."
type: docs
weight: 574
url: /ru/java/com.aspose.words/reportingengine/
---

**Inheritance:**
java.lang.Object
```
public class ReportingEngine
```

Предоставляет процедуры для заполнения шаблонных документов данными и набор настроек для управления этими процедурами.

Чтобы узнать больше, посетите статью документации [ LINQ Reporting Engine ][LINQ Reporting Engine].


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [ReportingEngine()](#ReportingEngine) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [buildReport(Document document, Object dataSource)](#buildReport-com.aspose.words.Document-java.lang.Object) | Заполняет указанный шаблонный документ данными из указанного источника, делая его готовым отчетом. |
| [buildReport(Document document, Object dataSource, String dataSourceName)](#buildReport-com.aspose.words.Document-java.lang.Object-java.lang.String) | Заполняет указанный шаблонный документ данными из указанного источника, делая его готовым отчетом. |
| [buildReport(Document document, Object[] dataSources, String[] dataSourceNames)](#buildReport-com.aspose.words.Document-java.lang.Object---java.lang.String) | Заполняет указанный шаблонный документ данными из указанных источников, делая его готовым отчетом. |
| [equals(Object obj)](#equals-java.lang.Object) |  |
| [getKnownTypes()](#getKnownTypes) | Получает неупорядоченный набор (т.е. |
| [getMissingMemberMessage()](#getMissingMemberMessage) | Получает строковое значение, выводимое вместо шаблонного выражения, представляющего простую ссылку на отсутствующий член объекта. |
| [getOptions()](#getOptions) | Получает набор флагов, контролирующих поведение этого экземпляра [ReportingEngine](../../com.aspose.words/reportingengine/) при построении отчёта. |
| [getRestrictedTypes()](#getRestrictedTypes) | Возвращает типы, чьи члены, а также члены производных типов, должны быть недоступны движку через синтаксис шаблона. |
| [getUseReflectionOptimization()](#getUseReflectionOptimization) | Получает значение, указывающее, оптимизированы ли вызовы пользовательских членов типов, выполненные через API рефлексии, с использованием динамической генерации классов или нет. |
| [hashCode()](#hashCode) |  |
| [setMissingMemberMessage(String value)](#setMissingMemberMessage-java.lang.String) | Устанавливает строковое значение, выводимое вместо шаблонного выражения, представляющего простую ссылку на отсутствующий член объекта. |
| [setOptions(int value)](#setOptions-int) | Устанавливает набор флагов, контролирующих поведение этого экземпляра [ReportingEngine](../../com.aspose.words/reportingengine/) при построении отчёта. |
| [setRestrictedTypes(Class[] types)](#setRestrictedTypes-java.lang.Class...) | Указывает типы, чьи члены, а также члены производных типов, должны быть недоступны движку через синтаксис шаблона. |
| [setUseReflectionOptimization(boolean value)](#setUseReflectionOptimization-boolean) | Устанавливает значение, указывающее, оптимизированы ли вызовы пользовательских членов типов, выполненные через API рефлексии, с использованием динамической генерации классов или нет. |
### ReportingEngine() {#ReportingEngine}
```
public ReportingEngine()
```


Инициализирует новый экземпляр этого класса.

### buildReport(Document document, Object dataSource) {#buildReport-com.aspose.words.Document-java.lang.Object}
```
public boolean buildReport(Document document, Object dataSource)
```


Заполняет указанный шаблонный документ данными из указанного источника, делая его готовым отчетом.

 **Remarks:** 

Используя эту перегрузку, вы можете ссылаться на члены источника данных в шаблонном документе, но не можете ссылаться на сам объект источника данных. Вы должны использовать перегрузку [buildReport(com.aspose.words.Document, java.lang.Object, java.lang.String)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object--java.lang.String) для достижения этого.

Объект источника данных может быть одного из следующих типов:

 *  [XmlDataSource](../../com.aspose.words/xmldatasource/)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource/)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource/)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset/)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable/)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow/)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader/)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
 *  [DataView](../../com.aspose.words.net.system.data/dataview/)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview/)
 *  Any other arbitrary Java type

Для получения информации о работе с источниками данных разных типов в шаблонных документах см. справочник по синтаксису шаблонов (https://docs.aspose.com/display/wordsjava/Template+Syntax).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Шаблонный документ, который будет заполнен данными. |
| dataSource | java.lang.Object | Объект источника данных. |

**Returns:**
boolean - Флаг, указывающий, успешно ли выполнен разбор шаблонного документа. Возвращаемый флаг имеет смысл только если значение свойства [getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) включает опцию [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions/\#INLINE-ERROR-MESSAGES).
### buildReport(Document document, Object dataSource, String dataSourceName) {#buildReport-com.aspose.words.Document-java.lang.Object-java.lang.String}
```
public boolean buildReport(Document document, Object dataSource, String dataSourceName)
```


Заполняет указанный шаблонный документ данными из указанного источника, делая его готовым отчетом.

 **Remarks:** 

Используя эту перегрузку, вы можете ссылаться на члены источника данных и сам объект источника данных в шаблоне. Если вы не собираетесь ссылаться на сам объект источника данных, вы можете опустить  dataSourceName , передав  null , или использовать перегрузку [buildReport(com.aspose.words.Document, java.lang.Object)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object).

Объект источника данных может быть одного из следующих типов:

 *  [XmlDataSource](../../com.aspose.words/xmldatasource/)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource/)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource/)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset/)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable/)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow/)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader/)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
 *  [DataView](../../com.aspose.words.net.system.data/dataview/)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview/)
 *  Any other arbitrary Java type

Для получения информации о работе с источниками данных разных типов в шаблонных документах см. справочник по синтаксису шаблонов (https://docs.aspose.com/display/wordsjava/Template+Syntax).

 **Examples:** 

Показывает, как разрешить отсутствующие члены.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

Показывает, как отображать значения в виде долларового текста.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("<<[ds.getValue1()]:dollarText>>\r<<[ds.getValue2()]:dollarText>>");

 NumericTestClass testData = new NumericTestBuilder().withValues(1234, 5621718.589).build();

 ReportingEngine report = new ReportingEngine();
 report.getKnownTypes().add(NumericTestClass.class);
 report.buildReport(doc, testData, "ds");

 doc.save(getArtifactsDir() + "ReportingEngine.DollarTextFormat.docx");
 
```

Показывает, как избирательно удалять абзацы.

```

 // Template contains tags with an exclamation mark. For such tags, empty paragraphs will be removed.
 Document doc = new Document(getMyDir() + "Reporting engine template - Selective remove paragraphs.docx");

 ReportingEngine engine = new ReportingEngine();
 engine.buildReport(doc, false, "value");

 doc.save(getArtifactsDir() + "ReportingEngine.SelectiveDeletionOfParagraphs.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Шаблонный документ, который будет заполнен данными. |
| dataSource | java.lang.Object | Объект источника данных. |
| dataSourceName | java.lang.String | Имя для ссылки на объект источника данных в шаблоне. |

**Returns:**
boolean - Флаг, указывающий, успешно ли выполнен разбор шаблонного документа. Возвращаемый флаг имеет смысл только если значение свойства [getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) включает опцию [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions/\#INLINE-ERROR-MESSAGES).
### buildReport(Document document, Object[] dataSources, String[] dataSourceNames) {#buildReport-com.aspose.words.Document-java.lang.Object---java.lang.String}
```
public boolean buildReport(Document document, Object[] dataSources, String[] dataSourceNames)
```


Заполняет указанный шаблонный документ данными из указанных источников, делая его готовым отчетом.

 **Remarks:** 

Используя эту перегрузку, вы можете ссылаться на несколько объектов источников данных и их члены в шаблоне. Имя первого источника данных может быть опущено (т.е. быть пустой строкой или  null ), если вы собираетесь ссылаться на члены источника данных, но не на сам объект источника данных. Имена остальных источников данных должны быть указаны и уникальны.

Если вы собираетесь использовать один источник данных, рассмотрите возможность использования перегрузок [buildReport(com.aspose.words.Document, java.lang.Object)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object) и [buildReport(com.aspose.words.Document, java.lang.Object, java.lang.String)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object--java.lang.String) вместо этого.

Объект источника данных может быть одного из следующих типов:

 *  [XmlDataSource](../../com.aspose.words/xmldatasource/)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource/)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource/)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset/)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable/)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow/)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader/)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
 *  [DataView](../../com.aspose.words.net.system.data/dataview/)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview/)
 *  Any other arbitrary Java type

Для получения информации о работе с источниками данных разных типов в шаблонных документах см. справочник по синтаксису шаблонов (https://docs.aspose.com/display/wordsjava/Template+Syntax).

 **Examples:** 

Показывает, как сохранить вставленную нумерацию без изменений.

```

 // By default, numbered lists from a template document are continued when their identifiers match those from a document being inserted.
 // With "-sourceNumbering" numbering should be separated and kept as is.
 Document template = DocumentHelper.createSimpleDocument("<>" + System.lineSeparator() + "<>");

 DocumentTestClass doc = new DocumentTestBuilder()
         .withDocument(new Document(getMyDir() + "List item.docx")).build();

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.REMOVE_EMPTY_PARAGRAPHS); }
 engine.buildReport(template, new Object[] { doc }, new String[] { "src" });

 template.save(getArtifactsDir() + "ReportingEngine.SourseListNumbering.docx");
 
```

Показывает, как работать с диаграммами из Word 2016.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Word 2016 Charts (Java).docx");

 ReportingEngine engine = new ReportingEngine();
 engine.buildReport(doc, new Object[] { Common.getShares(), Common.getShareQuotes() },
         new String[] { "shares", "quotes" });

 doc.save(getArtifactsDir() + "ReportingEngine.Word2016Charts.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Шаблонный документ, который будет заполнен данными. |
| dataSources | java.lang.Object[] | Массив объектов источников данных. |
| dataSourceNames | java.lang.String[] | Массив имён для ссылки на объекты источников данных в шаблоне. |

**Returns:**
boolean - Флаг, указывающий, успешно ли выполнен разбор шаблонного документа. Возвращаемый флаг имеет смысл только если значение свойства [getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) включает опцию [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions/\#INLINE-ERROR-MESSAGES).
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getKnownTypes() {#getKnownTypes}
```
public KnownTypeSet getKnownTypes()
```


Получает неупорядоченный набор (т.е. коллекцию уникальных элементов), содержащий объекты java.lang.Class, полные или частичные имена которых могут использоваться в шаблонах отчётов, обрабатываемых этим экземпляром движка, для вызова статических членов соответствующих типов, выполнения приведения типов и т.д.

**Returns:**
[KnownTypeSet](../../com.aspose.words/knowntypeset/) - An unordered set (i.e.
### getMissingMemberMessage() {#getMissingMemberMessage}
```
public String getMissingMemberMessage()
```


Получает строковое значение, выводимое вместо шаблонного выражения, представляющего простую ссылку на отсутствующий член объекта. Значение по умолчанию — пустая строка.

 **Remarks:** 

Это свойство следует использовать вместе с опцией [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS). В противном случае будет выброшено исключение, когда будет обнаружен отсутствующий член объекта.

Это свойство влияет только на вывод шаблонного выражения, представляющего простую ссылку на отсутствующий член объекта. Например, вывод бинарного оператора, один из операндов которого ссылается на отсутствующий член объекта, не затрагивается.

Значение этого свойства не может быть установлено в null.

 **Examples:** 

Показывает, как разрешить отсутствующие члены.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

**Returns:**
java.lang.String — строковое значение, выводимое вместо шаблонного выражения, представляющего простую ссылку на отсутствующий член объекта.
### getOptions() {#getOptions}
```
public int getOptions()
```


Получает набор флагов, контролирующих поведение этого экземпляра [ReportingEngine](../../com.aspose.words/reportingengine/) при построении отчёта.

 **Examples:** 

Показывает, как разрешить отсутствующие члены.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

Показывает, как установить параметры для Reporting Engine

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Fields (Java).docx");

 // Note that enabling of the option makes the engine to update fields while building a report,
 // so there is no need to update fields separately after that.
 ReportingEngine engine = new ReportingEngine();
 engine.setOptions(ReportBuildOptions.UPDATE_FIELDS_SYNTAX_AWARE);
 engine.buildReport(doc, new String[] { "First topic", "Second topic", "Third topic" }, "topics");

 doc.save(getArtifactsDir() + "ReportingEngine.UpdateFieldsSyntaxAware.docx");
 
```

**Returns:**
int — набор флагов, контролирующих поведение этого [ReportingEngine](../../com.aspose.words/reportingengine/) при построении отчёта. Возвращаемое значение представляет собой побитовое сочетание констант [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/).
### getRestrictedTypes() {#getRestrictedTypes}
```
public static Class[] getRestrictedTypes()
```


Возвращает типы, чьи члены, а также члены производных типов, должны быть недоступны движку через синтаксис шаблона.

 **Remarks:** 

Возвращаемый массив содержит элементы, ранее установленные с помощью [setRestrictedTypes(java.lang.Class[])](../../com.aspose.words/reportingengine/\#setRestrictedTypes-java.lang.Class).

Изменение элементов возвращаемого массива не влияет на ограниченные типы. Чтобы изменить ограниченные типы, используйте [setRestrictedTypes(java.lang.Class[])](../../com.aspose.words/reportingengine/\#setRestrictedTypes-java.lang.Class) вместо этого.

**Returns:**
java.lang.Class[] - Типы, чьи члены, а также члены производных типов, должны быть недоступны движку через синтаксис шаблона.
### getUseReflectionOptimization() {#getUseReflectionOptimization}
```
public static boolean getUseReflectionOptimization()
```


Возвращает значение, указывающее, оптимизируются ли вызовы членов пользовательских типов, выполненные через API рефлексии, с помощью динамической генерации классов. Значение по умолчанию —  true .

 **Remarks:** 

Существуют сценарии, когда предпочтительно отключить эту оптимизацию. Например, если вы постоянно работаете с небольшими коллекциями элементов данных, то накладные расходы на динамическую генерацию классов могут быть более заметными, чем накладные расходы на прямые вызовы API рефлексии. Параметр не действует при запуске на iOS, и оптимизация рефлексии не используется.

**Returns:**
boolean - Значение, указывающее, оптимизируются ли вызовы членов пользовательских типов, выполненные через API рефлексии, с помощью динамической генерации классов.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### setMissingMemberMessage(String value) {#setMissingMemberMessage-java.lang.String}
```
public void setMissingMemberMessage(String value)
```


Устанавливает строковое значение, выводимое вместо шаблонного выражения, представляющего простую ссылку на отсутствующий член объекта. Значение по умолчанию — пустая строка.

 **Remarks:** 

Это свойство следует использовать вместе с опцией [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS). В противном случае будет выброшено исключение, когда будет обнаружен отсутствующий член объекта.

Это свойство влияет только на вывод шаблонного выражения, представляющего простую ссылку на отсутствующий член объекта. Например, вывод бинарного оператора, один из операндов которого ссылается на отсутствующий член объекта, не затрагивается.

Значение этого свойства не может быть установлено в null.

 **Examples:** 

Показывает, как разрешить отсутствующие члены.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Строковое значение, выводимое вместо шаблонного выражения, представляющего простую ссылку на отсутствующий член объекта. |

### setOptions(int value) {#setOptions-int}
```
public void setOptions(int value)
```


Устанавливает набор флагов, контролирующих поведение этого экземпляра [ReportingEngine](../../com.aspose.words/reportingengine/) при построении отчёта.

 **Examples:** 

Показывает, как разрешить отсутствующие члены.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

Показывает, как установить параметры для Reporting Engine

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Fields (Java).docx");

 // Note that enabling of the option makes the engine to update fields while building a report,
 // so there is no need to update fields separately after that.
 ReportingEngine engine = new ReportingEngine();
 engine.setOptions(ReportBuildOptions.UPDATE_FIELDS_SYNTAX_AWARE);
 engine.buildReport(doc, new String[] { "First topic", "Second topic", "Third topic" }, "topics");

 doc.save(getArtifactsDir() + "ReportingEngine.UpdateFieldsSyntaxAware.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Набор флагов, контролирующих поведение этого [ReportingEngine](../../com.aspose.words/reportingengine/) при построении отчёта. Значение должно быть побитовым сочетанием констант [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/). |

### setRestrictedTypes(Class[] types) {#setRestrictedTypes-java.lang.Class...}
```
public static void setRestrictedTypes(Class[] types)
```


Указывает типы, чьи члены, а также члены производных типов, должны быть недоступны движку через синтаксис шаблона.

 **Remarks:** 

Ограниченные типы следует задавать до первой сборки отчета. После вызова  BuildReportbuildReport  ограниченные типы нельзя изменить, и при попытке сделать это будет выброшено исключение. Лучшее место для установки ограниченных типов — запуск приложения.

Обратите внимание, что большое количество ограниченных типов может влиять на производительность, поэтому лучше ограничивать только те типы, доступ к членам которых действительно чувствителен.

Выбрасывает java.lang.IllegalArgumentException в следующих случаях:

\-  types  равен null.

\- Один из элементов  types  равен null.

\- Один из элементов  types  представляет невидимый тип, то есть непубличный тип или публичный вложенный тип, у которого внешний тип непубличный.

\- Один из элементов  types  представляет тип массива.

\-  types  содержит дублирующие записи.

 **Examples:** 

Показывает, как запретить доступ к членам типов, считающихся небезопасными.

```

 Document doc =
         DocumentHelper.createSimpleDocument(
                 "<><<[typeVar]>>");

 // Note, that you can't set restricted types during or after building a report.
 ReportingEngine.setRestrictedTypes(Class.class);
 // We set "AllowMissingMembers" option to avoid exceptions during building a report.
 ReportingEngine engine = new ReportingEngine();
 engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
 engine.buildReport(doc, new Object());

 // We get an empty string because we can't access the GetType() method.
 Assert.assertEquals(doc.getText().trim(), "");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| types | java.lang.Class[] | Типы, которые следует ограничить. |

### setUseReflectionOptimization(boolean value) {#setUseReflectionOptimization-boolean}
```
public static void setUseReflectionOptimization(boolean value)
```


Устанавливает значение, указывающее, оптимизируются ли вызовы членов пользовательских типов, выполненные через API рефлексии, с помощью динамической генерации классов. Значение по умолчанию —  true .

 **Remarks:** 

Существуют сценарии, когда предпочтительно отключить эту оптимизацию. Например, если вы постоянно работаете с небольшими коллекциями элементов данных, то накладные расходы на динамическую генерацию классов могут быть более заметными, чем накладные расходы на прямые вызовы API рефлексии. Параметр не действует при запуске на iOS, и оптимизация рефлексии не используется.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Значение, указывающее, оптимизируются ли вызовы членов пользовательских типов, выполненные через API рефлексии, с помощью динамической генерации классов или нет. |

