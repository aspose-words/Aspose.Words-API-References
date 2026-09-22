---
title: "ReportBuilderOptions"
linktitle: "ReportBuilderOptions"
second_title: "Aspose.Words لـ Java"
description: "يمثل خيارات لوظيفة محرك تقارير LINQ في جافا."
type: docs
weight: 573
url: /ar/java/com.aspose.words/reportbuilderoptions/
---

**Inheritance:**
java.lang.Object
```
public class ReportBuilderOptions
```

يمثل الخيارات لوظيفة LINQ Reporting Engine.

 **Examples:** 

يظهر كيفية تعبئة المستند بالبيانات.

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
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [ReportBuilderOptions()](#ReportBuilderOptions) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getKnownTypes()](#getKnownTypes) | يحصل على مجموعة غير مرتبة (أي |
| [getMissingMemberMessage()](#getMissingMemberMessage) | يحصل على قيمة نصية مطبوعة بدلاً من تعبير القالب الذي يمثل إشارة بسيطة إلى عضو مفقود في كائن. |
| [getOptions()](#getOptions) | يحصل على مجموعة من العلامات التي تتحكم في سلوك هذه المثيلة من [ReportingEngine](../../com.aspose.words/reportingengine/) أثناء بناء التقرير. |
| [setMissingMemberMessage(String value)](#setMissingMemberMessage-java.lang.String) | يضبط قيمة نصية مطبوعة بدلاً من تعبير القالب الذي يمثل إشارة بسيطة إلى عضو مفقود في كائن. |
| [setOptions(int value)](#setOptions-int) | يضبط مجموعة من العلامات التي تتحكم في سلوك هذه المثيلة من [ReportingEngine](../../com.aspose.words/reportingengine/) أثناء بناء التقرير. |
### ReportBuilderOptions() {#ReportBuilderOptions}
```
public ReportBuilderOptions()
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

### getKnownTypes() {#getKnownTypes}
```
public KnownTypeSet getKnownTypes()
```


يحصل على مجموعة غير مرتبة (أي مجموعة من العناصر الفريدة) تحتوي على كائنات java.lang.Class التي يمكن استخدام أسمائها المؤهلة بالكامل أو جزئياً داخل قوالب التقارير التي يعالجها هذا المحرك لاستدعاء الأعضاء الثابتة للأنواع المقابلة، وإجراء تحويلات النوع، إلخ.

**Returns:**
[KnownTypeSet](../../com.aspose.words/knowntypeset/) - An unordered set (i.e.
### getMissingMemberMessage() {#getMissingMemberMessage}
```
public String getMissingMemberMessage()
```


يحصل على قيمة نصية مطبوعة بدلاً من تعبير القالب الذي يمثل إشارة بسيطة إلى عضو مفقود في كائن. القيمة الافتراضية هي سلسلة فارغة.

 **Remarks:** 

يجب استخدام الخاصية بالتزامن مع خيار [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS). وإلا، سيتم رمي استثناء عندما يُصادف عضو مفقود في كائن.

تؤثر الخاصية فقط على طباعة تعبير القالب الذي يمثل إشارة بسيطة إلى عضو مفقود في كائن. على سبيل المثال، طباعة عامل ثنائي يكون أحد معامله يشير إلى عضو مفقود في كائن لا تتأثر.

لا يمكن تعيين قيمة هذه الخاصية إلى null.

**Returns:**
java.lang.String - قيمة نصية مطبوعة بدلاً من تعبير القالب الذي يمثل إشارة بسيطة إلى عضو مفقود في كائن.
### getOptions() {#getOptions}
```
public int getOptions()
```


يحصل على مجموعة من العلامات التي تتحكم في سلوك هذه المثيلة من [ReportingEngine](../../com.aspose.words/reportingengine/) أثناء بناء التقرير.

 **Examples:** 

يظهر كيفية تعبئة المستند بالبيانات.

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
int - مجموعة من العلامات التي تتحكم في سلوك هذه المثيلة من [ReportingEngine](../../com.aspose.words/reportingengine/) أثناء بناء التقرير. القيمة المرجعة هي تركيبة بتية من ثوابت [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/).
### setMissingMemberMessage(String value) {#setMissingMemberMessage-java.lang.String}
```
public void setMissingMemberMessage(String value)
```


يضبط قيمة نصية مطبوعة بدلاً من تعبير القالب الذي يمثل إشارة بسيطة إلى عضو مفقود في كائن. القيمة الافتراضية هي سلسلة فارغة.

 **Remarks:** 

يجب استخدام الخاصية بالتزامن مع خيار [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS). وإلا، سيتم رمي استثناء عندما يُصادف عضو مفقود في كائن.

تؤثر الخاصية فقط على طباعة تعبير القالب الذي يمثل إشارة بسيطة إلى عضو مفقود في كائن. على سبيل المثال، طباعة عامل ثنائي يكون أحد معامله يشير إلى عضو مفقود في كائن لا تتأثر.

لا يمكن تعيين قيمة هذه الخاصية إلى null.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | قيمة نصية مطبوعة بدلاً من تعبير القالب الذي يمثل إشارة بسيطة إلى عضو مفقود في كائن. |

### setOptions(int value) {#setOptions-int}
```
public void setOptions(int value)
```


يضبط مجموعة من العلامات التي تتحكم في سلوك هذه المثيلة من [ReportingEngine](../../com.aspose.words/reportingengine/) أثناء بناء التقرير.

 **Examples:** 

يظهر كيفية تعبئة المستند بالبيانات.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | مجموعة من العلامات التي تتحكم في سلوك هذه المثيلة من [ReportingEngine](../../com.aspose.words/reportingengine/) أثناء بناء التقرير. يجب أن تكون القيمة تركيبة بتية من ثوابت [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/). |

