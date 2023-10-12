---
title: ReportingEngine.BuildReport
second_title: Aspose.Words لمراجع .NET API
description: ReportingEngine طريقة. يملأ مستند القالب المحدد بالبيانات من المصدر المحدد مما يجعله تقريرًا جاهزًا.
type: docs
weight: 40
url: /ar/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(Document, object) {#buildreport}

يملأ مستند القالب المحدد بالبيانات من المصدر المحدد مما يجعله تقريرًا جاهزًا.

```csharp
public bool BuildReport(Document document, object dataSource)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| document | Document | مستند نموذجي ليتم ملؤه بالبيانات. |
| dataSource | Object | كائن مصدر البيانات. |

### قيمة الإرجاع

علامة تشير إلى ما إذا كان تحليل مستند القالب ناجحًا. تكون العلامة التي تم إرجاعها منطقية فقط إذا كانت قيمة[`Options`](../options/)تتضمن الخاصية وInlineErrorMessages خيار.

### ملاحظات

باستخدام هذا التحميل الزائد يمكنك الإشارة إلى أعضاء مصدر البيانات في مستند القالب، لكن لا يمكنك الإشارة إلى كائن مصدر البيانات نفسه. يجب عليك استخدام`BuildReport` التحميل الزائد لتحقيق ذلك.

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
* أي نوع .NET تعسفي آخر غير ديناميكي وغير مجهول

للحصول على معلومات حول كيفية العمل مع مصادر البيانات من أنواع مختلفة في مستندات القالب، راجع مرجع بناء جملة القالب (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### أنظر أيضا

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* مساحة الاسم [Aspose.Words.Reporting](../../reportingengine/)
* المجسم [Aspose.Words](../../../)

---

## BuildReport(Document, object, string) {#buildreport_1}

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

علامة تشير إلى ما إذا كان تحليل مستند القالب ناجحًا. تكون العلامة التي تم إرجاعها منطقية فقط إذا كانت قيمة[`Options`](../options/)تتضمن الخاصية وInlineErrorMessages خيار.

### ملاحظات

باستخدام هذا التحميل الزائد يمكنك الرجوع إلى أعضاء مصدر البيانات وكائن مصدر البيانات نفسه في القالب. إذا كنت لن تقوم بالإشارة إلى كائن مصدر البيانات نفسه، فيمكنك حذفه*dataSourceName* عابر`باطل` أو استخدم`BuildReport` الزائد.

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
* أي نوع .NET تعسفي آخر غير ديناميكي وغير مجهول

للحصول على معلومات حول كيفية العمل مع مصادر البيانات من أنواع مختلفة في مستندات القالب، راجع مرجع بناء جملة القالب (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### أنظر أيضا

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* مساحة الاسم [Aspose.Words.Reporting](../../reportingengine/)
* المجسم [Aspose.Words](../../../)

---

## BuildReport(Document, object[], string[]) {#buildreport_2}

يملأ مستند القالب المحدد بالبيانات من المصادر المحددة مما يجعله تقريرًا جاهزًا.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| document | Document | مستند نموذجي ليتم ملؤه بالبيانات. |
| dataSources | Object[] | صفيف من كائنات مصدر البيانات. |
| dataSourceNames | String[] | صفيف من الأسماء للإشارة إلى كائنات مصدر البيانات داخل القالب. |

### قيمة الإرجاع

علامة تشير إلى ما إذا كان تحليل مستند القالب ناجحًا. تكون العلامة التي تم إرجاعها منطقية فقط إذا كانت قيمة[`Options`](../options/)تتضمن الخاصية وInlineErrorMessages خيار.

### ملاحظات

باستخدام هذا التحميل الزائد يمكنك الرجوع إلى كائنات مصدر بيانات متعددة وأعضائها في القالب. يمكن حذف اسم مصدر البيانات الأول (أي أن يكون سلسلة فارغة أو`باطل` إذا كنت ستقوم بالإشارة إلى إلى أعضاء مصدر البيانات وليس إلى كائن مصدر البيانات نفسه. يجب أن تكون أسماء مصادر البيانات الأخرى محددة وفريدة من نوعها.

إذا كنت ستستخدم مصدر بيانات واحدًا، ففكر في استخدام of`BuildReport` و`BuildReport` الأحمال الزائدة بدلاً من ذلك.

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
* أي نوع .NET تعسفي آخر غير ديناميكي وغير مجهول

للحصول على معلومات حول كيفية العمل مع مصادر البيانات من أنواع مختلفة في مستندات القالب، راجع مرجع بناء جملة القالب (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### أنظر أيضا

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* مساحة الاسم [Aspose.Words.Reporting](../../reportingengine/)
* المجسم [Aspose.Words](../../../)


