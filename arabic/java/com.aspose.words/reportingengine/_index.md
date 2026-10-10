---
title: "ReportingEngine"
linktitle: "ReportingEngine"
second_title: "Aspose.Words لـ Java"
description: "يوفر روتينات لملء مستندات القوالب بالبيانات ومجموعة من الإعدادات للتحكم في هذه الروتينات في Java."
type: docs
weight: 574
url: /ar/java/com.aspose.words/reportingengine/
---

**Inheritance:**
java.lang.Object
```
public class ReportingEngine
```

يوفر روتينات لملء مستندات القالب بالبيانات ومجموعة من الإعدادات للتحكم في هذه الروتينات.

للتعرف على المزيد، زر مقالة توثيق [ LINQ Reporting Engine ][LINQ Reporting Engine].


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [ReportingEngine()](#ReportingEngine) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [buildReport(Document document, Object dataSource)](#buildReport-com.aspose.words.Document-java.lang.Object) | يملأ مستند القالب المحدد بالبيانات من المصدر المحدد مما يجعله تقريرًا جاهزًا. |
| [buildReport(Document document, Object dataSource, String dataSourceName)](#buildReport-com.aspose.words.Document-java.lang.Object-java.lang.String) | يملأ مستند القالب المحدد بالبيانات من المصدر المحدد مما يجعله تقريرًا جاهزًا. |
| [buildReport(Document document, Object[] dataSources, String[] dataSourceNames)](#buildReport-com.aspose.words.Document-java.lang.Object---java.lang.String) | يملأ مستند القالب المحدد بالبيانات من المصادر المحددة مما يجعله تقريرًا جاهزًا. |
| [equals(Object obj)](#equals-java.lang.Object) |  |
| [getKnownTypes()](#getKnownTypes) | يحصل على مجموعة غير مرتبة (أي |
| [getMissingMemberMessage()](#getMissingMemberMessage) | يحصل على قيمة نصية مطبوعة بدلاً من تعبير القالب الذي يمثل إشارة بسيطة إلى عضو مفقود في كائن. |
| [getOptions()](#getOptions) | يحصل على مجموعة من العلامات التي تتحكم في سلوك هذه المثيلة من [ReportingEngine](../../com.aspose.words/reportingengine/) أثناء بناء التقرير. |
| [getRestrictedTypes()](#getRestrictedTypes) | يرجع الأنواع التي يجب أن تكون أعضاؤها وأعضاء الأنواع المشتقة غير قابلة للوصول من قبل المحرك عبر صياغة القالب. |
| [getUseReflectionOptimization()](#getUseReflectionOptimization) | يحصل على قيمة تشير إلى ما إذا كانت استدعاءات أعضاء النوع المخصص التي تُجرى عبر واجهة برمجة تطبيقات الانعكاس مُحسّنة باستخدام توليد فئة ديناميكي أم لا. |
| [hashCode()](#hashCode) |  |
| [setMissingMemberMessage(String value)](#setMissingMemberMessage-java.lang.String) | يضبط قيمة نصية مطبوعة بدلاً من تعبير القالب الذي يمثل إشارة بسيطة إلى عضو مفقود في كائن. |
| [setOptions(int value)](#setOptions-int) | يضبط مجموعة من العلامات التي تتحكم في سلوك هذه المثيلة من [ReportingEngine](../../com.aspose.words/reportingengine/) أثناء بناء التقرير. |
| [setRestrictedTypes(Class[] types)](#setRestrictedTypes-java.lang.Class...) | يحدد الأنواع التي يجب أن تكون أعضاؤها وأعضاء الأنواع المشتقة غير قابلة للوصول من قبل المحرك عبر صياغة القالب. |
| [setUseReflectionOptimization(boolean value)](#setUseReflectionOptimization-boolean) | يضبط قيمة تشير إلى ما إذا كانت استدعاءات أعضاء النوع المخصص التي تُجرى عبر واجهة برمجة تطبيقات الانعكاس مُحسّنة باستخدام توليد فئة ديناميكي أم لا. |
### ReportingEngine() {#ReportingEngine}
```
public ReportingEngine()
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

### buildReport(Document document, Object dataSource) {#buildReport-com.aspose.words.Document-java.lang.Object}
```
public boolean buildReport(Document document, Object dataSource)
```


يملأ مستند القالب المحدد بالبيانات من المصدر المحدد مما يجعله تقريرًا جاهزًا.

 **Remarks:** 

باستخدام هذا التحميل الزائد يمكنك الإشارة إلى أعضاء مصدر البيانات في مستند القالب، ولكن لا يمكنك الإشارة إلى كائن مصدر البيانات نفسه. يجب عليك استخدام التحميل الزائد [buildReport(com.aspose.words.Document, java.lang.Object, java.lang.String)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object--java.lang.String) لتحقيق ذلك.

يمكن أن يكون كائن مصدر البيانات أحد الأنواع التالية:

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

للحصول على معلومات حول كيفية العمل مع مصادر البيانات ذات الأنواع المختلفة في مستندات القالب، راجع مرجع صياغة القالب (https://docs.aspose.com/display/wordsjava/Template+Syntax).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | مستند قالب ليتم ملؤه بالبيانات. |
| dataSource | java.lang.Object | كائن مصدر بيانات. |

**Returns:**
boolean - علامة تشير إلى ما إذا كان تحليل مستند القالب ناجحًا. تكون العلامة المرتجعة ذات معنى فقط إذا كانت قيمة الخاصية [getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) تشمل خيار [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions/\#INLINE-ERROR-MESSAGES).
### buildReport(Document document, Object dataSource, String dataSourceName) {#buildReport-com.aspose.words.Document-java.lang.Object-java.lang.String}
```
public boolean buildReport(Document document, Object dataSource, String dataSourceName)
```


يملأ مستند القالب المحدد بالبيانات من المصدر المحدد مما يجعله تقريرًا جاهزًا.

 **Remarks:** 

باستخدام هذا التحميل الزائد يمكنك الإشارة إلى أعضاء مصدر البيانات وكائن مصدر البيانات نفسه في القالب. إذا لم تكن تنوي الإشارة إلى كائن مصدر البيانات نفسه، يمكنك حذف  dataSourceName  وتمرير  null  أو استخدام التحميل الزائد [buildReport(com.aspose.words.Document, java.lang.Object)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object).

يمكن أن يكون كائن مصدر البيانات أحد الأنواع التالية:

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

للحصول على معلومات حول كيفية العمل مع مصادر البيانات ذات الأنواع المختلفة في مستندات القالب، راجع مرجع صياغة القالب (https://docs.aspose.com/display/wordsjava/Template+Syntax).

 **Examples:** 

يعرض كيفية السماح بالأعضاء المفقودة.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

يعرض كيفية عرض القيم كنص دولار.

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

يعرض كيفية إزالة الفقرات بشكل انتقائي.

```

 // Template contains tags with an exclamation mark. For such tags, empty paragraphs will be removed.
 Document doc = new Document(getMyDir() + "Reporting engine template - Selective remove paragraphs.docx");

 ReportingEngine engine = new ReportingEngine();
 engine.buildReport(doc, false, "value");

 doc.save(getArtifactsDir() + "ReportingEngine.SelectiveDeletionOfParagraphs.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | مستند قالب ليتم ملؤه بالبيانات. |
| dataSource | java.lang.Object | كائن مصدر بيانات. |
| dataSourceName | java.lang.String | اسم للإشارة إلى كائن مصدر البيانات في القالب. |

**Returns:**
boolean - علامة تشير إلى ما إذا كان تحليل مستند القالب ناجحًا. تكون العلامة المرتجعة ذات معنى فقط إذا كانت قيمة الخاصية [getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) تشمل خيار [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions/\#INLINE-ERROR-MESSAGES).
### buildReport(Document document, Object[] dataSources, String[] dataSourceNames) {#buildReport-com.aspose.words.Document-java.lang.Object---java.lang.String}
```
public boolean buildReport(Document document, Object[] dataSources, String[] dataSourceNames)
```


يملأ مستند القالب المحدد بالبيانات من المصادر المحددة مما يجعله تقريرًا جاهزًا.

 **Remarks:** 

باستخدام هذا التحميل الزائد يمكنك الإشارة إلى كائنات متعددة لمصدر البيانات وأعضائها في القالب. يمكن حذف اسم مصدر البيانات الأول (أي أن يكون سلسلة فارغة أو  null ) إذا كنت ستشير إلى أعضاء مصدر البيانات ولكن ليس إلى كائن مصدر البيانات نفسه. يجب تحديد أسماء مصادر البيانات الأخرى وتكون فريدة.

إذا كنت ستستخدم مصدر بيانات واحد، ففكر في استخدام التحميل الزائد [buildReport(com.aspose.words.Document, java.lang.Object)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object) و [buildReport(com.aspose.words.Document, java.lang.Object, java.lang.String)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object--java.lang.String) بدلاً من ذلك.

يمكن أن يكون كائن مصدر البيانات أحد الأنواع التالية:

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

للحصول على معلومات حول كيفية العمل مع مصادر البيانات ذات الأنواع المختلفة في مستندات القالب، راجع مرجع صياغة القالب (https://docs.aspose.com/display/wordsjava/Template+Syntax).

 **Examples:** 

يعرض كيفية الحفاظ على الترقيم المدخل كما هو.

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

يعرض كيفية العمل مع المخططات من Word 2016.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Word 2016 Charts (Java).docx");

 ReportingEngine engine = new ReportingEngine();
 engine.buildReport(doc, new Object[] { Common.getShares(), Common.getShareQuotes() },
         new String[] { "shares", "quotes" });

 doc.save(getArtifactsDir() + "ReportingEngine.Word2016Charts.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | مستند قالب ليتم ملؤه بالبيانات. |
| dataSources | java.lang.Object[] | مصفوفة من كائنات مصدر البيانات. |
| dataSourceNames | java.lang.String[] | مصفوفة من الأسماء للإشارة إلى كائنات مصدر البيانات داخل القالب. |

**Returns:**
boolean - علامة تشير إلى ما إذا كان تحليل مستند القالب ناجحًا. تكون العلامة المرتجعة ذات معنى فقط إذا كانت قيمة الخاصية [getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) تشمل خيار [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions/\#INLINE-ERROR-MESSAGES).
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
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

 **Examples:** 

يعرض كيفية السماح بالأعضاء المفقودة.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

**Returns:**
java.lang.String - قيمة نصية مطبوعة بدلاً من تعبير القالب الذي يمثل إشارة بسيطة إلى عضو مفقود في كائن.
### getOptions() {#getOptions}
```
public int getOptions()
```


يحصل على مجموعة من العلامات التي تتحكم في سلوك هذه المثيلة من [ReportingEngine](../../com.aspose.words/reportingengine/) أثناء بناء التقرير.

 **Examples:** 

يعرض كيفية السماح بالأعضاء المفقودة.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

يوضح كيفية ضبط الخيارات لمحرك التقارير

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
int - مجموعة من العلامات التي تتحكم في سلوك هذه المثيلة من [ReportingEngine](../../com.aspose.words/reportingengine/) أثناء بناء التقرير. القيمة المرجعة هي تركيبة بتية من ثوابت [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/).
### getRestrictedTypes() {#getRestrictedTypes}
```
public static Class[] getRestrictedTypes()
```


يرجع الأنواع التي يجب أن تكون أعضاؤها وأعضاء الأنواع المشتقة غير قابلة للوصول من قبل المحرك عبر صياغة القالب.

 **Remarks:** 

المصفوفة المعادة تحتوي على عناصر تم ضبطها مسبقًا باستخدام [setRestrictedTypes(java.lang.Class[])](../../com.aspose.words/reportingengine/\#setRestrictedTypes-java.lang.Class).

تغيير عناصر المصفوفة المعادة لا يؤثر على الأنواع المقيدة. لتغيير الأنواع المقيدة، استخدم [setRestrictedTypes(java.lang.Class[])](../../com.aspose.words/reportingengine/\#setRestrictedTypes-java.lang.Class) بدلاً من ذلك.

**Returns:**
java.lang.Class[] - الأنواع التي يجب أن تكون أعضاؤها وكذلك أعضاء الأنواع المشتقة غير قابلة للوصول من قبل المحرك عبر صياغة القالب.
### getUseReflectionOptimization() {#getUseReflectionOptimization}
```
public static boolean getUseReflectionOptimization()
```


يحصل على قيمة تشير إلى ما إذا كانت استدعاءات أعضاء النوع المخصص التي تُجرى عبر واجهة برمجة تطبيقات الانعكاس مُحسّنة باستخدام توليد فئات ديناميكي أم لا. القيمة الافتراضية هي  true .

 **Remarks:** 

هناك بعض السيناريوهات التي يُفضَّل فيها تعطيل هذا التحسين. على سبيل المثال، إذا كنت تتعامل دائمًا مع مجموعات صغيرة من عناصر البيانات، فإن تكلفة توليد الفئات الديناميكي قد تكون أكثر وضوحًا من تكلفة استدعاءات واجهة برمجة تطبيقات الانعكاس المباشرة. لا يؤثر هذا الخيار عند التشغيل على iOS ولا يتم استخدام تحسين الانعكاس.

**Returns:**
boolean - قيمة تشير إلى ما إذا كانت استدعاءات أعضاء النوع المخصص التي تُجرى عبر واجهة برمجة تطبيقات الانعكاس مُحسّنة باستخدام توليد فئات ديناميكي أم لا.
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


يضبط قيمة نصية مطبوعة بدلاً من تعبير القالب الذي يمثل إشارة بسيطة إلى عضو مفقود في كائن. القيمة الافتراضية هي سلسلة فارغة.

 **Remarks:** 

يجب استخدام الخاصية بالتزامن مع خيار [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS). وإلا، سيتم رمي استثناء عندما يُصادف عضو مفقود في كائن.

تؤثر الخاصية فقط على طباعة تعبير القالب الذي يمثل إشارة بسيطة إلى عضو مفقود في كائن. على سبيل المثال، طباعة عامل ثنائي يكون أحد معامله يشير إلى عضو مفقود في كائن لا تتأثر.

لا يمكن تعيين قيمة هذه الخاصية إلى null.

 **Examples:** 

يعرض كيفية السماح بالأعضاء المفقودة.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

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

يعرض كيفية السماح بالأعضاء المفقودة.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

يوضح كيفية ضبط الخيارات لمحرك التقارير

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | مجموعة من العلامات التي تتحكم في سلوك هذه المثيلة من [ReportingEngine](../../com.aspose.words/reportingengine/) أثناء بناء التقرير. يجب أن تكون القيمة تركيبة بتية من ثوابت [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/). |

### setRestrictedTypes(Class[] types) {#setRestrictedTypes-java.lang.Class...}
```
public static void setRestrictedTypes(Class[] types)
```


يحدد الأنواع التي يجب أن تكون أعضاؤها وأعضاء الأنواع المشتقة غير قابلة للوصول من قبل المحرك عبر صياغة القالب.

 **Remarks:** 

يجب ضبط الأنواع المقيدة قبل أول بناء لتقرير. بعد استدعاء  BuildReportbuildReport ، لا يمكن تعديل الأنواع المقيدة وسيتم رمي استثناء عند محاولة القيام بذلك. أفضل مكان لضبط الأنواع المقيدة هو بدء تشغيل التطبيق.

لاحظ أن عددًا كبيرًا من الأنواع المقيدة قد يؤثر على الأداء، لذا من الأفضل تقييد تلك الأنواع فقط التي يكون الوصول إلى أعضائها حساسًا حقًا.

يرمي java.lang.IllegalArgumentException في الحالات التالية:

\-  types  فارغ.

\- أحد عناصر  types  فارغ.

\- أحد عناصر  types  يمثل نوعًا غير مرئي، أي نوع غير عام أو نوع متداخل عام له نوع خارجي غير عام.

\- أحد عناصر  types  يمثل نوع مصفوفة.

\-  types  يحتوي على إدخالات مكررة.

 **Examples:** 

يوضح كيفية رفض الوصول إلى أعضاء الأنواع التي تُعتبر غير آمنة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| الأنواع | java.lang.Class[] | الأنواع التي يجب تقييدها. |

### setUseReflectionOptimization(boolean value) {#setUseReflectionOptimization-boolean}
```
public static void setUseReflectionOptimization(boolean value)
```


يضبط قيمة تشير إلى ما إذا كانت استدعاءات أعضاء النوع المخصص التي تُجرى عبر واجهة برمجة تطبيقات الانعكاس مُحسّنة باستخدام توليد فئات ديناميكي أم لا. القيمة الافتراضية هي  true .

 **Remarks:** 

هناك بعض السيناريوهات التي يُفضَّل فيها تعطيل هذا التحسين. على سبيل المثال، إذا كنت تتعامل دائمًا مع مجموعات صغيرة من عناصر البيانات، فإن تكلفة توليد الفئات الديناميكي قد تكون أكثر وضوحًا من تكلفة استدعاءات واجهة برمجة تطبيقات الانعكاس المباشرة. لا يؤثر هذا الخيار عند التشغيل على iOS ولا يتم استخدام تحسين الانعكاس.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة تشير إلى ما إذا كانت استدعاءات أعضاء النوع المخصص التي تُجرى عبر واجهة برمجة تطبيقات الانعكاس مُحسّنة باستخدام توليد فئات ديناميكي أم لا. |

