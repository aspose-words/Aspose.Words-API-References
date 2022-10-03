---
title: BuildReport
second_title: Aspose.Words لمراجع .NET API
description: يملأ مستند النموذج المحدد بالبيانات من المصدر المحدد مما يجعله تقريرًا جاهزًا.
type: docs
weight: 40
url: /ar/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(Document, object) {#buildreport}

يملأ مستند النموذج المحدد بالبيانات من المصدر المحدد مما يجعله تقريرًا جاهزًا.

```csharp
public bool BuildReport(Document document, object dataSource)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| document | Document | مستند نموذج يتم ملؤه بالبيانات. |
| dataSource | Object | كائن مصدر البيانات. |

### قيمة الإرجاع

علامة تشير إلى ما إذا كان تحليل مستند النموذج ناجحًا.[`Options`](../options/)تشمل الخاصية الInlineErrorMessages اختيار.

### ملاحظات

باستخدام هذا التحميل الزائد ، يمكنك الرجوع إلى أعضاء مصدر البيانات في مستند القالب ، ولكن لا يمكنك الإشارة إلى كائن مصدر البيانات نفسه. يجب عليك استخدام ملف[`BuildReport`](./buildreport/) الزائد لتحقيق ذلك.

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
* أي نوع تعسفي آخر غير ديناميكي وغير مجهول. NET type

للحصول على معلومات حول كيفية العمل مع مصادر البيانات من أنواع مختلفة في مستندات النموذج ، راجع مرجع بنية القالب (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### أنظر أيضا

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* مساحة الاسم [Aspose.Words.Reporting](../../reportingengine/)
* المجسم [Aspose.Words](../../../)

---

## BuildReport(Document, object, string) {#buildreport_1}

يملأ مستند النموذج المحدد بالبيانات من المصدر المحدد مما يجعله تقريرًا جاهزًا.

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| document | Document | مستند نموذج يتم ملؤه بالبيانات. |
| dataSource | Object | كائن مصدر البيانات. |
| dataSourceName | String | اسم للإشارة إلى كائن مصدر البيانات في القالب. |

### قيمة الإرجاع

علامة تشير إلى ما إذا كان تحليل مستند النموذج ناجحًا.[`Options`](../options/)تشمل الخاصية الInlineErrorMessages اختيار.

### ملاحظات

باستخدام هذا التحميل الزائد ، يمكنك الرجوع إلى أعضاء مصدر البيانات وكائن مصدر البيانات نفسه في القالب. إذا كنت لا تنوي الرجوع إلى كائن مصدر البيانات نفسه ، فيمكنك حذفه*dataSourceName* تمرير فارغ أو استخدام[`BuildReport`](./buildreport/) الزائد .

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
* أي نوع تعسفي آخر غير ديناميكي وغير مجهول. NET type

للحصول على معلومات حول كيفية العمل مع مصادر البيانات من أنواع مختلفة في مستندات النموذج ، راجع مرجع بنية القالب (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### أنظر أيضا

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* مساحة الاسم [Aspose.Words.Reporting](../../reportingengine/)
* المجسم [Aspose.Words](../../../)

---

## BuildReport(Document, object[], string[]) {#buildreport_2}

يملأ مستند النموذج المحدد بالبيانات من المصادر المحددة مما يجعله تقريرًا جاهزًا.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| document | Document | مستند نموذج يتم ملؤه بالبيانات. |
| dataSources | Object[] | مصفوفة من كائنات مصدر البيانات. |
| dataSourceNames | String[] | مصفوفة أسماء للإشارة إلى كائنات مصدر البيانات داخل القالب. |

### قيمة الإرجاع

علامة تشير إلى ما إذا كان تحليل مستند النموذج ناجحًا.[`Options`](../options/)تشمل الخاصية الInlineErrorMessages اختيار.

### ملاحظات

باستخدام هذا التحميل الزائد ، يمكنك الرجوع إلى كائنات مصدر بيانات متعددة وأعضائها في القالب. يمكن حذف اسم مصدر البيانات الأول (أي أن تكون سلسلة فارغة أو خالية) إذا كنت تريد الإشارة إلى أعضاء مصدر البيانات وليس إلى كائن مصدر البيانات نفسه. يجب تحديد أسماء مصادر البيانات الأخرى وفريدة من نوعها.

إذا كنت ستستخدم مصدر بيانات واحدًا ، ففكر في استخدام[`BuildReport`](./buildreport/) و[`BuildReport`](./buildreport/) الزائدة بدلا من ذلك.

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
* أي نوع تعسفي آخر غير ديناميكي وغير مجهول. NET type

للحصول على معلومات حول كيفية العمل مع مصادر البيانات من أنواع مختلفة في مستندات النموذج ، راجع مرجع بنية القالب (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### أنظر أيضا

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* مساحة الاسم [Aspose.Words.Reporting](../../reportingengine/)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
