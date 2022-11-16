---
title: ReportingEngine
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет подпрограммы для заполнения документов-шаблонов данными и набор параметров для управления этими подпрограммами.
type: docs
weight: 478
url: /ru/java/com.aspose.words/reportingengine/
---

**Наследование:**
java.lang.Object
```
public class ReportingEngine
```

Предоставляет подпрограммы для заполнения документов-шаблонов данными и набор параметров для управления этими подпрограммами.

 Чтобы узнать больше, посетите**LINQ Reporting Engine** документальная статья.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [ReportingEngine()](#ReportingEngine--) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [buildReport(Document document, Object dataSource)](#buildReport-com.aspose.words.Document-java.lang.Object-) | Заполняет указанный шаблонный документ данными из указанного источника, превращая его в готовый отчет. |
| [buildReport(Document document, Object dataSource, String dataSourceName)](#buildReport-com.aspose.words.Document-java.lang.Object-java.lang.String-) | Заполняет указанный шаблонный документ данными из указанного источника, превращая его в готовый отчет. |
| [buildReport(Document document, Object[] dataSources, String[] dataSourceNames)](#buildReport-com.aspose.words.Document-java.lang.Object---java.lang.String---) | Заполняет указанный шаблонный документ данными из указанных источников, превращая его в готовый отчет. |
| [equals(Object obj)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getKnownTypes()](#getKnownTypes--) | Получает неупорядоченный набор (т.е. |
| [getOptions()](#getOptions--) |  Получает набор флагов, управляющих поведением этого[ReportingEngine](../../com.aspose.words/reportingengine)экземпляр при построении отчета. |
| [getUseReflectionOptimization()](#getUseReflectionOptimization--) | Получает значение, указывающее, оптимизированы ли вызовы членов пользовательского типа, выполняемые через API отражения, с использованием динамического создания классов или нет. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setOptions(int value)](#setOptions-int-) |  Устанавливает набор флагов, управляющих поведением этого[ReportingEngine](../../com.aspose.words/reportingengine)экземпляр при построении отчета. |
| [setUseReflectionOptimization(boolean value)](#setUseReflectionOptimization-boolean-) | Задает значение, указывающее, оптимизированы ли вызовы членов пользовательского типа, выполняемые через API отражения, с использованием динамического создания классов или нет. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ReportingEngine() {#ReportingEngine--}
```
public ReportingEngine()
```


Инициализирует новый экземпляр этого класса.

### buildReport(Document document, Object dataSource) {#buildReport-com.aspose.words.Document-java.lang.Object-}
```
public boolean buildReport(Document document, Object dataSource)
```


Заполняет указанный шаблонный документ данными из указанного источника, превращая его в готовый отчет.

 Используя эту перегрузку, вы можете ссылаться на элементы источника данных в документе шаблона, но не можете ссылаться на сам объект источника данных. Вы должны использовать[buildReport(com.aspose.words.Document, java.lang.Object, java.lang.String)](../../com.aspose.words/reportingengine\#buildReport-com.aspose.words.Document--java.lang.Object--java.lang.String-) перегрузить для достижения этого.

Объект источника данных может быть одного из следующих типов:

 *  [XmlDataSource](../../com.aspose.words/xmldatasource)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord)
 *  [DataView](../../com.aspose.words.net.system.data/dataview)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview)
 *  Любой другой произвольный тип Java

Сведения о том, как работать с источниками данных разных типов в шаблонных документах, см. в справочнике по синтаксису шаблонов (https://docs.aspose.com/display/wordsjava/Template+Syntax).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document) | Шаблон документа для заполнения данными. |
| dataSource | java.lang.Object | Объект источника данных. |

**Возвращает:**
boolean — Флаг, указывающий, был ли разбор документа шаблона успешным. Возвращаемый флаг имеет смысл, только если значение[getOptions()](../../com.aspose.words/reportingengine\#getOptions--) / [setOptions(int)](../../com.aspose.words/reportingengine\#setOptions-int-) собственность включает в себя[ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions\#INLINE-ERROR-MESSAGES) вариант.
### buildReport(Document document, Object dataSource, String dataSourceName) {#buildReport-com.aspose.words.Document-java.lang.Object-java.lang.String-}
```
public boolean buildReport(Document document, Object dataSource, String dataSourceName)
```


Заполняет указанный шаблонный документ данными из указанного источника, превращая его в готовый отчет.

 Используя эту перегрузку, вы можете ссылаться на элементы источника данных и сам объект источника данных в шаблоне. Если вы не собираетесь ссылаться на сам объект источника данных, вы можете опустить dataSourceName, передавая null, или использовать[buildReport(com.aspose.words.Document, java.lang.Object)](../../com.aspose.words/reportingengine\#buildReport-com.aspose.words.Document--java.lang.Object-) перегрузка.

Объект источника данных может быть одного из следующих типов:

 *  [XmlDataSource](../../com.aspose.words/xmldatasource)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord)
 *  [DataView](../../com.aspose.words.net.system.data/dataview)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview)
 *  Любой другой произвольный тип Java

Сведения о том, как работать с источниками данных разных типов в шаблонных документах, см. в справочнике по синтаксису шаблонов (https://docs.aspose.com/display/wordsjava/Template+Syntax).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document) | Шаблон документа для заполнения данными. |
| dataSource | java.lang.Object | Объект источника данных. |
| dataSourceName | java.lang.String | Имя для ссылки на объект источника данных в шаблоне. |

**Возвращает:**
boolean — Флаг, указывающий, был ли разбор документа шаблона успешным. Возвращаемый флаг имеет смысл, только если значение[getOptions()](../../com.aspose.words/reportingengine\#getOptions--) / [setOptions(int)](../../com.aspose.words/reportingengine\#setOptions-int-) собственность включает в себя[ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions\#INLINE-ERROR-MESSAGES) вариант.
### buildReport(Document document, Object[] dataSources, String[] dataSourceNames) {#buildReport-com.aspose.words.Document-java.lang.Object---java.lang.String---}
```
public boolean buildReport(Document document, Object[] dataSources, String[] dataSourceNames)
```


Заполняет указанный шаблонный документ данными из указанных источников, превращая его в готовый отчет.

Используя эту перегрузку, вы можете ссылаться на несколько объектов источника данных и их членов в шаблоне. Имя первого источника данных может быть опущено (т. е. быть пустой строкой или нулевым значением), если вы собираетесь ссылаться на элементы источника данных, но не на сам объект источника данных. Имена других источников данных должны быть указаны и уникальны.

 Если вы собираетесь использовать один источник данных, рассмотрите возможность использования[buildReport(com.aspose.words.Document, java.lang.Object)](../../com.aspose.words/reportingengine\#buildReport-com.aspose.words.Document--java.lang.Object-) а также[buildReport(com.aspose.words.Document, java.lang.Object, java.lang.String)](../../com.aspose.words/reportingengine\#buildReport-com.aspose.words.Document--java.lang.Object--java.lang.String-) вместо этого перегружается.

Объект источника данных может быть одного из следующих типов:

 *  [XmlDataSource](../../com.aspose.words/xmldatasource)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord)
 *  [DataView](../../com.aspose.words.net.system.data/dataview)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview)
 *  Любой другой произвольный тип Java

Сведения о том, как работать с источниками данных разных типов в шаблонных документах, см. в справочнике по синтаксису шаблонов (https://docs.aspose.com/display/wordsjava/Template+Syntax).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document) | Шаблон документа для заполнения данными. |
| dataSources | java.lang.Object[] | Массив объектов источника данных. |
| dataSourceNames | java.lang.String[] | Массив имен для ссылки на объекты источника данных в шаблоне. |

**Возвращает:**
boolean — Флаг, указывающий, был ли разбор документа шаблона успешным. Возвращаемый флаг имеет смысл, только если значение[getOptions()](../../com.aspose.words/reportingengine\#getOptions--) / [setOptions(int)](../../com.aspose.words/reportingengine\#setOptions-int-) собственность включает в себя[ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions\#INLINE-ERROR-MESSAGES) вариант.
### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Возвращает:**
логический
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getKnownTypes() {#getKnownTypes--}
```
public KnownTypeSet getKnownTypes()
```


Получает неупорядоченный набор (т. е. набор уникальных элементов), содержащий объекты java.lang.Class, полностью или частично определенные имена которых могут использоваться в шаблонах отчетов, обрабатываемых этим экземпляром механизма, для вызова статических членов соответствующих типов, выполнения приведения типов и т. д. .

**Возвращает:**
[KnownTypeSet](../../com.aspose.words/knowntypeset) - Неупорядоченный набор (т.е.
### getOptions() {#getOptions--}
```
public int getOptions()
```


 Получает набор флагов, управляющих поведением этого[ReportingEngine](../../com.aspose.words/reportingengine)экземпляр при построении отчета.

**Возвращает:**
 int - Набор флагов, управляющих поведением этого[ReportingEngine](../../com.aspose.words/reportingengine) экземпляр при построении отчета. Возвращаемое значение представляет собой побитовую комбинацию[ReportBuildOptions](../../com.aspose.words/reportbuildoptions) константы.
### getUseReflectionOptimization() {#getUseReflectionOptimization--}
```
public static boolean getUseReflectionOptimization()
```


Получает значение, указывающее, оптимизированы ли вызовы членов пользовательского типа, выполняемые через API отражения, с использованием динамического создания классов или нет. Значение по умолчанию верно. Есть несколько сценариев, в которых предпочтительнее отключить эту оптимизацию. Например, если вы постоянно имеете дело с небольшими коллекциями элементов данных, то накладные расходы на создание динамического класса могут быть более заметными, чем накладные расходы на вызовы API прямого отражения. Параметр не действует при запуске на iOS, и оптимизация отражения не используется.

**Возвращает:**
логическое значение — значение, указывающее, оптимизированы ли вызовы членов пользовательского типа, выполняемые через API отражения, с использованием динамического создания классов или нет.
### hashCode() {#hashCode--}
```
public int hashCode()
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




### setOptions(int value) {#setOptions-int-}
```
public void setOptions(int value)
```


 Устанавливает набор флагов, управляющих поведением этого[ReportingEngine](../../com.aspose.words/reportingengine)экземпляр при построении отчета.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Набор флагов, управляющих поведением этого[ReportingEngine](../../com.aspose.words/reportingengine) экземпляр при построении отчета. Значение должно быть побитовой комбинацией[ReportBuildOptions](../../com.aspose.words/reportbuildoptions) константы. |

### setUseReflectionOptimization(boolean value) {#setUseReflectionOptimization-boolean-}
```
public static void setUseReflectionOptimization(boolean value)
```


Задает значение, указывающее, оптимизированы ли вызовы членов пользовательского типа, выполняемые через API отражения, с использованием динамического создания классов или нет. Значение по умолчанию верно. Есть несколько сценариев, в которых предпочтительнее отключить эту оптимизацию. Например, если вы постоянно имеете дело с небольшими коллекциями элементов данных, то накладные расходы на создание динамического класса могут быть более заметными, чем накладные расходы на вызовы API прямого отражения. Параметр не действует при запуске на iOS, и оптимизация отражения не используется.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, указывающее, оптимизированы ли вызовы членов настраиваемого типа, выполняемые через API отражения, с помощью создания динамического класса или нет. |

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
