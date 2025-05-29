---
title: ReportingEngine.BuildReport
linktitle: BuildReport
articleTitle: BuildReport
second_title: Aspose.Words لـ .NET
description: قم بإنشاء تقارير جاهزة للاستخدام بسهولة باستخدام طريقة BuildReport من ReportingEngine، وملء القوالب بسلاسة بالبيانات من المصدر الذي اخترته.
type: docs
weight: 50
url: /ar/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(*[Document](../../../aspose.words/document/), object*) {#buildreport}

يملأ مستند القالب المحدد بالبيانات من المصدر المحدد مما يجعله تقريرًا جاهزًا.

```csharp
public bool BuildReport(Document document, object dataSource)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| document | Document | مستند نموذجي ليتم ملؤه بالبيانات. |
| dataSource | Object | كائن مصدر البيانات. |

### قيمة الإرجاع

علم يشير إلى ما إذا كان تحليل مستند القالب ناجحًا أم لا. العلم الذي تم إرجاعه يكون منطقيًا فقط إذا كانت قيمة[`Options`](../options/) تتضمن الخاصية InlineErrorMessages خيار.

## ملاحظات

باستخدام هذا التحميل الزائد، يمكنك الرجوع إلى عناصر مصدر البيانات في مستند القالب، ولكن لا يمكنك الرجوع إلى كائن مصدر البيانات نفسه. يجب عليك استخدام`BuildReport` التحميل الزائد لتحقيق ذلك.

يمكن أن يكون كائن مصدر البيانات من أحد الأنواع التالية:

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* أي نوع آخر عشوائي غير ديناميكي وغير مجهول من نوع .NET

للحصول على معلومات حول كيفية العمل مع مصادر البيانات من أنواع مختلفة في مستندات القالب، راجع مرجع بناء جملة القالب (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### أنظر أيضا

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object, string*) {#buildreport_1}

يملأ مستند القالب المحدد بالبيانات من المصدر المحدد مما يجعله تقريرًا جاهزًا.

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| document | Document | مستند نموذجي ليتم ملؤه بالبيانات. |
| dataSource | Object | كائن مصدر البيانات. |
| dataSourceName | String | اسم للإشارة إلى كائن مصدر البيانات في القالب. |

### قيمة الإرجاع

علم يشير إلى ما إذا كان تحليل مستند القالب ناجحًا أم لا. العلم الذي تم إرجاعه يكون منطقيًا فقط إذا كانت قيمة[`Options`](../options/) تتضمن الخاصية InlineErrorMessages خيار.

## ملاحظات

باستخدام هذا التحميل الزائد، يمكنك الرجوع إلى أعضاء مصدر البيانات وكائن مصدر البيانات نفسه في القالب. إذا كنت لن تشير إلى كائن مصدر البيانات نفسه، فيمكنك حذفه*dataSourceName* يمر`باطل` أو استخدم`BuildReport` التحميل الزائد.

يمكن أن يكون كائن مصدر البيانات من أحد الأنواع التالية:

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* أي نوع آخر عشوائي غير ديناميكي وغير مجهول من نوع .NET

للحصول على معلومات حول كيفية العمل مع مصادر البيانات من أنواع مختلفة في مستندات القالب، راجع مرجع بناء جملة القالب (https://docs.aspose.com/display/wordsnet/Template+Syntax).

## أمثلة

يوضح كيفية السماح للأعضاء المفقودين.

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

يوضح كيفية إزالة الفقرات بشكل انتقائي.

```csharp
// يحتوي القالب على علامات تعجب. ستُحذف الفقرات الفارغة من هذه العلامات.
Document doc = new Document(MyDir + "Reporting engine template - Selective remove paragraphs.docx");

ReportingEngine engine = new ReportingEngine();
engine.BuildReport(doc, false, "value");

doc.Save(ArtifactsDir + "ReportingEngine.SelectiveDeletionOfParagraphs.docx");
```

يوضح كيفية عرض القيم كنص بالدولار.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("<<[ds.Value1]:dollarText>>\r<<[ds.Value2]:dollarText>>");

NumericTestClass testData = new NumericTestBuilder().WithValues(1234, 5621718.589).Build();

ReportingEngine report = new ReportingEngine();
report.KnownTypes.Add(typeof(NumericTestClass));
report.BuildReport(doc, testData, "ds");

doc.Save(ArtifactsDir + "ReportingEngine.DollarTextFormat.docx");
```

### أنظر أيضا

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object[], string[]*) {#buildreport_2}

يملأ مستند القالب المحدد بالبيانات من المصادر المحددة مما يجعله تقريرًا جاهزًا.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| document | Document | مستند نموذجي ليتم ملؤه بالبيانات. |
| dataSources | Object[] | مجموعة من كائنات مصدر البيانات. |
| dataSourceNames | String[] | مجموعة من الأسماء للإشارة إلى كائنات مصدر البيانات داخل القالب. |

### قيمة الإرجاع

علم يشير إلى ما إذا كان تحليل مستند القالب ناجحًا أم لا. العلم الذي تم إرجاعه يكون منطقيًا فقط إذا كانت قيمة[`Options`](../options/) تتضمن الخاصية InlineErrorMessages خيار.

## ملاحظات

باستخدام هذا التحميل الزائد، يمكنك الرجوع إلى كائنات مصدر بيانات متعددة وأعضائها في القالب. يمكن حذف اسم مصدر البيانات الأول (أي أن يكون سلسلة فارغة أو`باطل` إذا كنت ستشير إلى عناصر مصدر البيانات في وليس إلى كائن مصدر البيانات نفسه. يجب تحديد أسماء مصادر البيانات الأخرى في وأن تكون فريدة.

إذا كنت ستستخدم مصدر بيانات واحد، ففكر في استخدام`BuildReport` و`BuildReport` التحميل الزائد بدلا من ذلك.

يمكن أن يكون كائن مصدر البيانات من أحد الأنواع التالية:

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* أي نوع آخر عشوائي غير ديناميكي وغير مجهول من نوع .NET

للحصول على معلومات حول كيفية العمل مع مصادر البيانات من أنواع مختلفة في مستندات القالب، راجع مرجع بناء جملة القالب (https://docs.aspose.com/display/wordsnet/Template+Syntax).

## أمثلة

يوضح كيفية العمل مع المخططات البيانية من word 2016.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Word 2016 Charts.docx");

ReportingEngine engine = new ReportingEngine();
engine.BuildReport(doc, new object[] { Common.GetShares(), Common.GetShareQuotes() },
    new string[] { "shares", "quotes" });

doc.Save(ArtifactsDir + "ReportingEngine.Word2016Charts.docx");
```

يوضح كيفية الاحتفاظ بالترقيم المدرج كما هو.

```csharp
// بشكل افتراضي، تستمر القوائم المرقمة من مستند القالب عندما تتطابق معرفاتها مع تلك الموجودة في المستند الذي يتم إدراجه.
// باستخدام "-sourceNumbering" يجب فصل الترقيم والاحتفاظ به كما هو.
Document template = DocumentHelper.CreateSimpleDocument("<<doc [src.Document]>>" + Environment.NewLine + "<<doc [src.Document] -sourceNumbering>>");

DocumentTestClass doc = new DocumentTestBuilder()
    .WithDocument(new Document(MyDir + "List item.docx")).Build();

ReportingEngine engine = new ReportingEngine() { Options = ReportBuildOptions.RemoveEmptyParagraphs };
engine.BuildReport(template, new object[] { doc }, new[] { "src" });

template.Save(ArtifactsDir + "ReportingEngine.SourseListNumbering.docx");
```

### أنظر أيضا

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* مساحة الاسم [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* المجسم [Aspose.Words](../../../)
