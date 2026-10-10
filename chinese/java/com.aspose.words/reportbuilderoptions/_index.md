---
title: "ReportBuilderOptions"
linktitle: "ReportBuilderOptions"
second_title: "Aspose.Words for Java"
description: "表示 Java 中 LINQ 报告引擎功能的选项。"
type: docs
weight: 573
url: /zh/java/com.aspose.words/reportbuilderoptions/
---

**Inheritance:**
java.lang.Object
```
public class ReportBuilderOptions
```

表示 LINQ 报告引擎功能的选项。

 **Examples:** 

展示如何使用数据填充文档。

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
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [ReportBuilderOptions()](#ReportBuilderOptions) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [getKnownTypes()](#getKnownTypes) | 获取一个无序集合（即 |
| [getMissingMemberMessage()](#getMissingMemberMessage) | 获取在模板表达式位置打印的字符串值，以替代表示对象缺失成员的普通引用。 |
| [getOptions()](#getOptions) | 获取一组标志，用于控制此 [ReportingEngine](../../com.aspose.words/reportingengine/) 实例在生成报告时的行为。 |
| [setMissingMemberMessage(String value)](#setMissingMemberMessage-java.lang.String) | 设置在模板表达式位置打印的字符串值，以替代表示对象缺失成员的普通引用。 |
| [setOptions(int value)](#setOptions-int) | 设置一组标志，用于控制此 [ReportingEngine](../../com.aspose.words/reportingengine/) 实例在生成报告时的行为。 |
### ReportBuilderOptions() {#ReportBuilderOptions}
```
public ReportBuilderOptions()
```


初始化此类的新实例。

### getKnownTypes() {#getKnownTypes}
```
public KnownTypeSet getKnownTypes()
```


获取一个无序集合（即唯一项的集合），其中包含 java.lang.Class 对象，可在此引擎实例处理的报告模板中使用其完整或部分限定名称来调用相应类型的静态成员、执行类型转换等。

**Returns:**
[KnownTypeSet](../../com.aspose.words/knowntypeset/) - An unordered set (i.e.
### getMissingMemberMessage() {#getMissingMemberMessage}
```
public String getMissingMemberMessage()
```


获取在模板表达式位置打印的字符串值，以替代表示对象缺失成员的普通引用。默认值为空字符串。

 **Remarks:** 

该属性应与 [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS) 选项一起使用。否则，在遇到对象缺失成员时会抛出异常。

此属性仅影响打印表示对缺失对象成员的普通引用的模板表达式。例如，二元运算符的打印，其中一个操作数引用了缺失的对象成员，不受影响。

此属性的值不能设置为 null。

**Returns:**
java.lang.String - 用于替代表示对缺失对象成员的普通引用的模板表达式的字符串值。
### getOptions() {#getOptions}
```
public int getOptions()
```


获取一组标志，用于控制此 [ReportingEngine](../../com.aspose.words/reportingengine/) 实例在生成报告时的行为。

 **Examples:** 

展示如何使用数据填充文档。

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
int - 一组标志，用于控制在生成报告时此 [ReportingEngine](../../com.aspose.words/reportingengine/) 实例的行为。返回的值是 [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/) 常量的按位组合。
### setMissingMemberMessage(String value) {#setMissingMemberMessage-java.lang.String}
```
public void setMissingMemberMessage(String value)
```


设置用于替代表示对缺失对象成员的普通引用的模板表达式的字符串值。默认值为空字符串。

 **Remarks:** 

该属性应与 [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS) 选项一起使用。否则，在遇到对象缺失成员时会抛出异常。

此属性仅影响打印表示对缺失对象成员的普通引用的模板表达式。例如，二元运算符的打印，其中一个操作数引用了缺失的对象成员，不受影响。

此属性的值不能设置为 null。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 用于替代表示对缺失对象成员的普通引用的模板表达式的字符串值。 |

### setOptions(int value) {#setOptions-int}
```
public void setOptions(int value)
```


设置一组标志，用于控制此 [ReportingEngine](../../com.aspose.words/reportingengine/) 实例在生成报告时的行为。

 **Examples:** 

展示如何使用数据填充文档。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 一组标志，用于控制在生成报告时此 [ReportingEngine](../../com.aspose.words/reportingengine/) 实例的行为。该值必须是 [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/) 常量的按位组合。 |

