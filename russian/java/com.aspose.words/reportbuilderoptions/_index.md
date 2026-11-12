---
title: "ReportBuilderOptions"
linktitle: "ReportBuilderOptions"
second_title: "Aspose.Words для Java"
description: "Представляет параметры функциональности LINQ Reporting Engine в Java."
type: docs
weight: 573
url: /ru/java/com.aspose.words/reportbuilderoptions/
---

**Inheritance:**
java.lang.Object
```
public class ReportBuilderOptions
```

Представляет параметры для функциональности LINQ Reporting Engine.

 **Examples:** 

Показывает, как заполнить документ данными.

```

 public void buildReportData() throws Exception {
     // There is a several ways to populate document with data:
     String doc = getMyDir() + "Reporting engine template - If greedy (Java).docx";

     AsposeData obj = new AsposeData();
     {
         obj.setList(new ArrayList<>());
         {
             obj.getList().add("abc");
         }
     }

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.1.docx", obj);
     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.2.docx", obj, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.3.docx", SaveFormat.DOCX, obj);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.4.docx", SaveFormat.DOCX, obj, options);
 }

 public static class AsposeData {
     public ArrayList getList() {
         return mList;
     }

     ;

     public void setList(ArrayList value) {
         mList = value;
     }

     ;

     private ArrayList mList;
 }
 
```
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [ReportBuilderOptions()](#ReportBuilderOptions) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [getKnownTypes()](#getKnownTypes) | Получает неупорядоченный набор (т.е. |
| [getMissingMemberMessage()](#getMissingMemberMessage) | Получает строковое значение, выводимое вместо шаблонного выражения, представляющего простую ссылку на отсутствующий член объекта. |
| [getOptions()](#getOptions) | Получает набор флагов, контролирующих поведение этого экземпляра [ReportingEngine](../../com.aspose.words/reportingengine/) при построении отчёта. |
| [setMissingMemberMessage(String value)](#setMissingMemberMessage-java.lang.String) | Устанавливает строковое значение, выводимое вместо шаблонного выражения, представляющего простую ссылку на отсутствующий член объекта. |
| [setOptions(int value)](#setOptions-int) | Устанавливает набор флагов, контролирующих поведение этого экземпляра [ReportingEngine](../../com.aspose.words/reportingengine/) при построении отчёта. |
### ReportBuilderOptions() {#ReportBuilderOptions}
```
public ReportBuilderOptions()
```


Инициализирует новый экземпляр этого класса.

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

**Returns:**
java.lang.String — строковое значение, выводимое вместо шаблонного выражения, представляющего простую ссылку на отсутствующий член объекта.
### getOptions() {#getOptions}
```
public int getOptions()
```


Получает набор флагов, контролирующих поведение этого экземпляра [ReportingEngine](../../com.aspose.words/reportingengine/) при построении отчёта.

 **Examples:** 

Показывает, как заполнить документ данными.

```

 public void buildReportData() throws Exception {
     // There is a several ways to populate document with data:
     String doc = getMyDir() + "Reporting engine template - If greedy (Java).docx";

     AsposeData obj = new AsposeData();
     {
         obj.setList(new ArrayList<>());
         {
             obj.getList().add("abc");
         }
     }

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.1.docx", obj);
     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.2.docx", obj, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.3.docx", SaveFormat.DOCX, obj);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.4.docx", SaveFormat.DOCX, obj, options);
 }

 public static class AsposeData {
     public ArrayList getList() {
         return mList;
     }

     ;

     public void setList(ArrayList value) {
         mList = value;
     }

     ;

     private ArrayList mList;
 }
 
```

**Returns:**
int — набор флагов, контролирующих поведение этого [ReportingEngine](../../com.aspose.words/reportingengine/) при построении отчёта. Возвращаемое значение представляет собой побитовое сочетание констант [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/).
### setMissingMemberMessage(String value) {#setMissingMemberMessage-java.lang.String}
```
public void setMissingMemberMessage(String value)
```


Устанавливает строковое значение, выводимое вместо шаблонного выражения, представляющего простую ссылку на отсутствующий член объекта. Значение по умолчанию — пустая строка.

 **Remarks:** 

Это свойство следует использовать вместе с опцией [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS). В противном случае будет выброшено исключение, когда будет обнаружен отсутствующий член объекта.

Это свойство влияет только на вывод шаблонного выражения, представляющего простую ссылку на отсутствующий член объекта. Например, вывод бинарного оператора, один из операндов которого ссылается на отсутствующий член объекта, не затрагивается.

Значение этого свойства не может быть установлено в null.

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

Показывает, как заполнить документ данными.

```

 public void buildReportData() throws Exception {
     // There is a several ways to populate document with data:
     String doc = getMyDir() + "Reporting engine template - If greedy (Java).docx";

     AsposeData obj = new AsposeData();
     {
         obj.setList(new ArrayList<>());
         {
             obj.getList().add("abc");
         }
     }

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.1.docx", obj);
     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.2.docx", obj, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.3.docx", SaveFormat.DOCX, obj);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.4.docx", SaveFormat.DOCX, obj, options);
 }

 public static class AsposeData {
     public ArrayList getList() {
         return mList;
     }

     ;

     public void setList(ArrayList value) {
         mList = value;
     }

     ;

     private ArrayList mList;
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Набор флагов, контролирующих поведение этого [ReportingEngine](../../com.aspose.words/reportingengine/) при построении отчёта. Значение должно быть побитовым сочетанием констант [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/). |

