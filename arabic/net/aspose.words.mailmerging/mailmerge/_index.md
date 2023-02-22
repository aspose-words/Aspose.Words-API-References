---
title: Class MailMerge
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.MailMerging.MailMerge فصل. يمثل وظيفة دمج المراسلات.
type: docs
weight: 3620
url: /ar/net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

يمثل وظيفة دمج المراسلات.

```csharp
public class MailMerge
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions/) { get; set; } | الحصول على أو تعيين مجموعة من العلامات التي تحدد العناصر التي يجب إزالتها أثناء دمج المراسلات. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كانت الفقرات التي تحتوي على علامات ترقيم تعتبر فارغة ويجب إزالتها إذا كانRemoveEmptyParagraphs تم تحديد الخيار . |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback/) { get; set; } | يحدث أثناء دمج المراسلات عند مصادفة حقل دمج المراسلات في المستند. |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback/) { get; set; } | يسمح بمعالجة أحداث معينة أثناء دمج البريد. |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields/) { get; } | إرجاع مجموعة تمثل حقول البيانات المعينة لعملية دمج المراسلات. |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كان يجب دمج جميع مناطق دمج بريد المستندات مع اسم مصدر البيانات أثناء تنفيذ دمج البريد مع المناطق مقابل مصدر البيانات أو الأول فقط. |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كان سيتم تحديث الحقول في المستند بأكمله أثناء تنفيذ دمج البريد مع المناطق. |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كان يجب الاحتفاظ بعلامات "الشارب" غير المستخدمة . |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag/) { get; set; } | الحصول على علامة نهاية منطقة دمج المراسلات أو تعيينها. |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag/) { get; set; } | الحصول على علامة بدء منطقة دمج المراسلات أو تعيينها. |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كان سيتم إعادة تشغيل القوائم في كل قسم بعد تنفيذ عملية دمج البريد. |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كان ملف[`SectionStart`](../../aspose.words/pagesetup/sectionstart/) من قسم المستند الأول ونسخه لمصدر البيانات اللاحقة rows يتم الاحتفاظ بها أثناء دمج المراسلات أو تحديثها وفقًا لسلوك MS Word. |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كانت المسافات البيضاء الزائدة والبادئة قد تم اقتطاعها من قيم دمج البريد. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كانت حقول الدمج ومناطق الدمج مدمجة بغض النظر عن حالة حقل IF الأصلي. |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields/) { get; set; } | عندما يكون صحيحًا ، يحدد أنه بالإضافة إلى حقول MERGEFIELD ، يتم تنفيذ دمج المراسلات في بعض أنواع الحقول الأخرى و أيضًا في علامات "{{fieldName}}". |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كان يجب تضمين فقرة كاملة مع TableStart أو TableEnd field أو نطاق معين بين حقول TableStart و TableEnd في منطقة دمج المراسلات. |

## طُرق

| اسم | وصف |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields/)() | يزيل الحقول المتعلقة بدمج المراسلات من المستند. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_1)(DataRow) | تنفيذ دمج المراسلات من DataRow في المستند. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_2)(DataTable) | تنفيذ دمج المراسلات من DataTable في المستند. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_3)(DataView) | تنفيذ دمج البريد من DataView في المستند. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_4)(IDataReader) | تنفيذ دمج المراسلات من IDataReader في المستند. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute)(IMailMergeDataSource) | يقوم بإجراء دمج بريد من مصدر بيانات مخصص. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_5)(string[], object[]) | تنفيذ عملية دمج المراسلات لسجل واحد. |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado/)(object) | تنفيذ دمج المراسلات من كائن ADO Recordset في المستند. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_2)(DataSet) | تنفيذ دمج البريد من DataSet في مستند مع مناطق دمج المراسلات. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_3)(DataTable) | تنفيذ دمج المراسلات من DataTable في المستند مع مناطق دمج المراسلات. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_4)(DataView) | تنفيذ دمج المراسلات من DataView في المستند مع مناطق دمج المراسلات. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions)(IMailMergeDataSource) | يقوم بإجراء دمج بريد من مصدر بيانات مخصص بمناطق دمج البريد. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_1)(IMailMergeDataSourceRoot) | يقوم بإجراء دمج بريد من مصدر بيانات مخصص بمناطق دمج البريد. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_5)(IDataReader, string) | تنفيذ دمج المراسلات من IDataReader في المستند باستخدام مناطق دمج المراسلات. |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado/)(object, string) | تنفيذ دمج المراسلات من كائن ADO Recordset في المستند مع مناطق دمج المراسلات. |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames/)() | إرجاع مجموعة من أسماء حقول دمج المراسلات المتوفرة في المستند. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion)(string) | إرجاع مجموعة من أسماء حقول دمج المراسلات المتوفرة في المنطقة. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion_1)(string, int) | إرجاع مجموعة من أسماء حقول دمج المراسلات المتوفرة في المنطقة. |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname/)(string) | إرجاع مجموعة من مناطق دمج البريد بالاسم المحدد. |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy/)() | إرجاع تسلسل هرمي كامل للمناطق (مع الحقول) المتوفرة في المستند. |

### ملاحظات

لكي تعمل عملية دمج المراسلات ، يجب أن يحتوي المستند على Word MERGEFIELD و اختياريًا الحقول التالية. أثناء عملية دمج المراسلات ، يتم استبدال حقول الدمج في المستند بقيم من مصدر البيانات.

هناك طريقتان مميزتان لاستخدام دمج المراسلات: باستخدام مناطق دمج المراسلات وبدونها.

أبسط دمج للمراسلات هو بدون مناطق وهو مشابه جدًا لكيفية عمل دمج المراسلات في Word. يستخدمنفذ - اعدم طرق لدمج المعلومات من بعض مصادر البيانات مثل **جدول البيانات** و **مجموعة البيانات** و **عرض البيانات** و **إداتاريدر** أو مصفوفة من الكائنات في المستند الخاص بك. ال  **دمج المراسلات** يقوم الكائن بمعالجة جميع سجلات مصدر البيانات ونسخ وإلحاق محتوى المستند بأكمله لكل سجل.

لاحظ أن متى **دمج المراسلات**يواجه الكائن حقل NEXT ، ويحدد record التالي في مصدر البيانات ويستمر في الدمج دون نسخ أي محتوى.

يستخدمتنفيذيويث ريجيونس طرق لدمج المعلومات في مستند a بمناطق دمج المراسلات المحددة. يمكنك استخدام  **مجموعة البيانات** و **جدول البيانات** و **عرض البيانات** أو **إداتاريدر** كمصادر بيانات لهذه العملية.

تحتاج إلى استخدام مناطق دمج البريد إذا كنت تريد زيادة الأجزاء ديناميكيًا داخل المستند . بدون مناطق دمج المراسلات ، سيتم تكرار المستند بالكامل لكل سجل of لمصدر البيانات.

### أمثلة

يوضح كيفية تنفيذ دمج البريد مع البيانات من DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // فيما يلي طريقتان لاستخدام DataTable كمصدر بيانات لدمج البريد.
    // 1 - استخدم الجدول بأكمله لدمج البريد لإنشاء مستند دمج بريد ناتج واحد لكل صف في الجدول:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - استخدم صفًا واحدًا من الجدول لإنشاء مستند دمج بريد ناتج واحد:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// ينشئ مستند مصدر لدمج المراسلات.
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


