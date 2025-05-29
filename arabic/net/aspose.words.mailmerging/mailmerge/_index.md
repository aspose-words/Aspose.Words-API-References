---
title: MailMerge Class
linktitle: MailMerge
articleTitle: MailMerge
second_title: Aspose.Words لـ .NET
description: أطلق العنان لإمكانيات دمج البريد الإلكتروني الفعّالة مع فئة Aspose.Words.MailMerging.MailMerge. سهّل إنشاء المستندات وحسّن إنتاجيتك بسهولة!
type: docs
weight: 4530
url: /ar/net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

يمثل وظيفة دمج البريد.

لمعرفة المزيد، قم بزيارة[دمج البريد وإعداد التقارير](https://docs.aspose.com/words/net/mail-merge-and-reporting/) مقالة توثيقية.

```csharp
public class MailMerge
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions/) { get; set; } | يحصل على مجموعة من العلامات التي تحدد العناصر التي يجب إزالتها أثناء دمج البريد أو يعينها. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/) { get; set; } | يحصل على قيمة أو يعينها تشير إلى ما إذا كانت الفقرات التي تحتوي على علامات ترقيم تعتبر فارغة ويجب إزالتها إذاRemoveEmptyParagraphs تم تحديد الخيار. |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback/) { get; set; } | يحدث أثناء دمج البريد عند مواجهة حقل دمج البريد في المستند. |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback/) { get; set; } | يسمح بالتعامل مع أحداث معينة أثناء دمج البريد. |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields/) { get; } | يعيد مجموعة تمثل حقول البيانات المخصصة لعملية دمج البريد. |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions/) { get; set; } | يحصل على قيمة أو يعينها تشير إلى ما إذا كان يجب دمج جميع مناطق دمج البريد للمستندات التي تحمل اسم مصدر البيانات أثناء تنفيذ دمج البريد مع المناطق مقابل مصدر البيانات أو المنطقة الأولى فقط. |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument/) { get; set; } | يحصل على قيمة أو يعينها للإشارة إلى ما إذا كانت الحقول في المستند بأكمله يتم تحديثها أثناء تنفيذ دمج البريد مع المناطق. |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags/) { get; set; } | يحصل على قيمة تشير إلى ما إذا كان يجب الحفاظ على علامات "الشارب" غير المستخدمة أو تعيينها. |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag/) { get; set; } | يحصل على علامة نهاية منطقة دمج البريد أو يعينها. |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag/) { get; set; } | يحصل على علامة بدء منطقة دمج البريد أو يعينها. |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection/) { get; set; } | يحصل على قيمة أو يعينها للإشارة إلى ما إذا كان سيتم إعادة تشغيل القوائم في كل قسم بعد تنفيذ دمج البريد. |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart/) { get; set; } | يحصل على قيمة أو يعينها للإشارة إلى ما إذا كان[`SectionStart`](../../aspose.words/pagesetup/sectionstart/) يتم الاحتفاظ بقسم المستند الأول ونسخه لصفوف مصدر البيانات اللاحقة أثناء دمج البريد أو يتم تحديثها وفقًا لسلوك MS Word. |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces/) { get; set; } | يحصل على قيمة أو يعينها للإشارة إلى ما إذا كانت المسافات البيضاء النهائية والبادئة يتم اقتصاصها من قيم دمج البريد. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/) { get; set; } | يحصل على قيمة أو يعينها تشير إلى ما إذا كانت حقول الدمج ومناطق الدمج مدمجة بغض النظر عن حالة حقل IF الرئيسي. |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields/) { get; set; } | عندما`حقيقي` , يحدد أنه بالإضافة إلى حقول MERGEFIELD، يتم تنفيذ دمج البريد في بعض الأنواع الأخرى من الحقول و أيضًا في علامات "{{fieldName}}". |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/) { get; set; } | يحصل على قيمة أو يعينها للإشارة إلى ما إذا كانت الفقرة بأكملها تحتوي على**بدء تشغيل الجدول** أو**نهاية الجدول** field أو نطاق معين بين**بدء تشغيل الجدول** و**نهاية الجدول** يجب تضمين الحقول في منطقة دمج البريد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields/)() | يزيل الحقول المرتبطة بدمج البريد من المستند. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_1)(*DataRow*) | يقوم بدمج البريد من**صف البيانات** في المستند. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_2)(*DataTable*) | يقوم بدمج البريد من جدول بيانات إلى المستند. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_3)(*DataView*) | يقوم بدمج البريد من**عرض البيانات** في المستند. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_4)(*IDataReader*) | يقوم بدمج البريد من**قارئ بيانات الهوية** في المستند. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute)(*[IMailMergeDataSource](../imailmergedatasource/)*) | يقوم بتنفيذ دمج البريد من مصدر بيانات مخصص. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_5)(*string[], object[]*) | ينفذ عملية دمج البريد لسجل واحد. |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado/)(*object*) | يقوم بتنفيذ دمج البريد من كائن مجموعة سجلات ADO إلى المستند. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_2)(*DataSet*) | يقوم بدمج البريد من**مجموعة البيانات** في مستند يحتوي على مناطق دمج البريد. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_3)(*DataTable*) | يقوم بدمج البريد من**جدول البيانات** في المستند مع مناطق دمج البريد. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_4)(*DataView*) | يقوم بدمج البريد من**عرض البيانات** في المستند مع مناطق دمج البريد. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions)(*[IMailMergeDataSource](../imailmergedatasource/)*) | يقوم بتنفيذ دمج البريد من مصدر بيانات مخصص مع مناطق دمج البريد. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_1)(*[IMailMergeDataSourceRoot](../imailmergedatasourceroot/)*) | يقوم بتنفيذ دمج البريد من مصدر بيانات مخصص مع مناطق دمج البريد. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_5)(*IDataReader, string*) | يقوم بدمج البريد من**قارئ بيانات الهوية** في المستند مع مناطق دمج البريد. |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado/)(*object, string*) | يقوم بتنفيذ دمج البريد من كائن مجموعة سجلات ADO إلى المستند الذي يحتوي على مناطق دمج البريد. |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames/)() | يقوم بإرجاع مجموعة من أسماء حقول دمج البريد المتوفرة في المستند. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion)(*string*) | يقوم بإرجاع مجموعة من أسماء حقول دمج البريد المتوفرة في المنطقة. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion_1)(*string, int*) | يقوم بإرجاع مجموعة من أسماء حقول دمج البريد المتوفرة في المنطقة. |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname/)(*string*) | يعيد مجموعة من مناطق دمج البريد بالاسم المحدد. |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy/)() | يعيد التسلسل الهرمي الكامل للمناطق (مع الحقول) المتوفرة في المستند. |

## ملاحظات

لكي تعمل عملية دمج المراسلات، يجب أن يحتوي المستند على حقلي MERGEFIELD و (اختياريًا NEXT). أثناء عملية دمج المراسلات، تُستبدل حقول الدمج في المستند بقيم من مصدر بياناتك.

هناك طريقتان مختلفتان لاستخدام دمج البريد: مع مناطق دمج البريد وبدونها.

أبسط عملية دمج بريدي هي بدون مناطق، وهي مشابهة جدًا لكيفية عمل mail merge في Word. استخدمينفذ طرق لدمج المعلومات من مصدر بيانات some مثل**جدول البيانات** ،**مجموعة البيانات** ،**عرض البيانات** ،**قارئ بيانات الهوية** أو مجموعة من الكائنات في مستندك.`MailMerge` تعمل العملية على معالجة جميع سجلات مصدر البيانات ونسخ وإضافة محتوى المستند بأكمله لكل سجل.

لاحظ أنه عندما`MailMerge`عندما يواجه الكائن الحقل التالي، فإنه يحدد السجل التالي في مصدر البيانات ويستمر في الدمج دون نسخ أي محتوى.

يستخدم[`ExecuteWithRegions`](./executewithregions/) وغيرها من عمليات التحميل الزائد لدمج المعلومات في مستند a مع تحديد مناطق دمج البريد. يمكنك استخدام **مجموعة البيانات** ،**جدول البيانات** ،**عرض البيانات** أو**قارئ بيانات الهوية** كمصدر بيانات لهذه العملية.

يجب عليك استخدام مناطق دمج البريد إذا كنت ترغب في زيادة أجزاء داخل مستند ديناميكيًا. بدون مناطق دمج البريد، سيتم تكرار المستند بأكمله لكل سجل في مصدر البيانات .

## أمثلة

يوضح كيفية تنفيذ دمج البريد باستخدام البيانات من جدول البيانات.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // فيما يلي طريقتان لاستخدام جدول البيانات كمصدر بيانات لدمج البريد.
    // 1 - استخدم الجدول بأكمله لدمج البريد لإنشاء مستند دمج بريدي واحد لكل صف في الجدول:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - استخدم صفًا واحدًا من الجدول لإنشاء مستند دمج بريدي واحد:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// إنشاء مستند مصدر لدمج البريد.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../)
