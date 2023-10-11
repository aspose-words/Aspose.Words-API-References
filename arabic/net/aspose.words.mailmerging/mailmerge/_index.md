---
title: Class MailMerge
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.MailMerging.MailMerge فصل. يمثل وظيفة دمج البريد.
type: docs
weight: 3840
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
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions/) { get; set; } | الحصول على أو تعيين مجموعة من العلامات التي تحدد العناصر التي يجب إزالتها أثناء دمج البريد. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كانت الفقرات التي تحتوي على علامات ترقيم تعتبر فارغة ويجب إزالتها إذا كانتRemoveEmptyParagraphs تم تحديد الخيار. |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback/) { get; set; } | يحدث أثناء دمج البريد عند مواجهة حقل دمج البريد في المستند. |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback/) { get; set; } | يسمح بمعالجة أحداث معينة أثناء دمج البريد. |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields/) { get; } | إرجاع مجموعة تمثل حقول البيانات المعينة لعملية دمج البريد. |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كان يجب دمج كافة مناطق دمج مراسلات المستند التي تحمل اسم مصدر البيانات أثناء تنفيذ دمج البريد مع المناطق مقابل مصدر البيانات أو المصدر الأول فقط. |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument/) { get; set; } | الحصول على قيمة أو تعيينها تشير إلى ما إذا كان سيتم تحديث الحقول الموجودة في المستند بأكمله أثناء تنفيذ دمج البريد مع المناطق. |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كان يجب الاحتفاظ بعلامات "الشارب" غير المستخدمة. |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag/) { get; set; } | الحصول على علامة نهاية منطقة دمج البريد أو تعيينها. |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag/) { get; set; } | الحصول على علامة بدء منطقة دمج البريد أو تعيينها. |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كان سيتم إعادة تشغيل القوائم في كل قسم بعد تنفيذ عملية دمج البريد. |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كان[`SectionStart`](../../aspose.words/pagesetup/sectionstart/) من قسم المستند الأول ونسخه لصفوف مصدر البيانات اللاحقة يتم الاحتفاظ بها أثناء دمج البريد أو تحديثها وفقًا لسلوك MS Word. |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces/) { get; set; } | الحصول على قيمة أو تعيينها تشير إلى ما إذا كان سيتم اقتطاع المسافات البيضاء الزائدة والبادئة من قيم دمج المراسلات. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كان سيتم دمج حقول الدمج ومناطق الدمج بغض النظر عن حالة حقل IF الأصلي. |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields/) { get; set; } | متى`حقيقي` ، يحدد أنه بالإضافة إلى حقول MERGEFIELD، يتم إجراء دمج البريد في بعض أنواع الحقول الأخرى و أيضًا في علامات "{{fieldName}}". |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كانت الفقرة بأكملها بها **TableStart** أو **نهاية الجدول** field أو نطاق معين بين **TableStart** و **نهاية الجدول** يجب تضمين الحقول في منطقة دمج البريد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields/)() | إزالة الحقول المرتبطة بدمج البريد من المستند. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_1)(DataRow) | يقوم بدمج البريد من a **DataRow** في المستند. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_2)(DataTable) | تنفيذ دمج البريد من DataTable في المستند. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_3)(DataView) | يقوم بدمج البريد من a **عرض البيانات** في المستند. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_4)(IDataReader) | يقوم بدمج البريد من **معرف البيانات** في المستند. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute)(IMailMergeDataSource) | تنفيذ عملية دمج البريد من مصدر بيانات مخصص. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_5)(string[], object[]) | تنفيذ عملية دمج البريد لسجل واحد. |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado/)(object) | تنفيذ دمج البريد من كائن ADO Recordset في المستند. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_2)(DataSet) | يقوم بدمج البريد من a **DataSet** في مستند يحتوي على مناطق دمج البريد. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_3)(DataTable) | يقوم بدمج البريد من a **جدول البيانات** في المستند الذي يحتوي على مناطق دمج البريد. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_4)(DataView) | يقوم بدمج البريد من a **عرض البيانات** في المستند الذي يحتوي على مناطق دمج البريد. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions)(IMailMergeDataSource) | تنفيذ عملية دمج البريد من مصدر بيانات مخصص مع مناطق دمج البريد. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_1)(IMailMergeDataSourceRoot) | تنفيذ عملية دمج البريد من مصدر بيانات مخصص مع مناطق دمج البريد. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_5)(IDataReader, string) | يقوم بدمج البريد من **معرف البيانات** في المستند الذي يحتوي على مناطق دمج البريد. |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado/)(object, string) | إجراء دمج البريد من كائن ADO Recordset في المستند باستخدام مناطق دمج البريد. |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames/)() | إرجاع مجموعة من أسماء حقول دمج المراسلات المتوفرة في المستند. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion)(string) | إرجاع مجموعة من أسماء حقول دمج المراسلات المتوفرة في المنطقة. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion_1)(string, int) | إرجاع مجموعة من أسماء حقول دمج المراسلات المتوفرة في المنطقة. |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname/)(string) | إرجاع مجموعة من مناطق دمج البريد بالاسم المحدد. |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy/)() | يُرجع التسلسل الهرمي الكامل للمناطق (مع الحقول) المتوفرة في المستند. |

### ملاحظات

لكي تعمل عملية دمج البريد، يجب أن يحتوي المستند على حقول Word MERGEFIELD و اختياريًا NEXT. أثناء عملية دمج البريد، يتم استبدال حقول الدمج في المستند بقيم من مصدر البيانات.

هناك طريقتان مختلفتان لاستخدام دمج البريد: مع مناطق دمج البريد وبدونها.

أبسط عملية دمج للبريد هي بدون مناطق وهي مشابهة جدًا لكيفية عمل mail merge في Word. يستخدمينفذ طرق لدمج المعلومات من مصدر بيانات some مثل **جدول البيانات** , **DataSet** , **عرض البيانات** , **معرف البيانات** أو مجموعة من الكائنات في المستند الخاص بك. The `MailMerge` يعالج الكائن كافة سجلات مصدر البيانات وينسخ محتوى المستند بالكامل ويلحقه بكل سجل.

لاحظ أنه عندما`MailMerge` عندما يواجه الكائن حقل NEXT، فإنه يحدد السجل التالي في مصدر البيانات ويستمر في الدمج دون نسخ أي محتوى.

يستخدم[`ExecuteWithRegions`](./executewithregions/) والأحمال الزائدة الأخرى لدمج المعلومات في مستند a مع تحديد مناطق دمج البريد. يمكنك استخدام  **DataSet** , **جدول البيانات** , **عرض البيانات** أو **معرف البيانات** كمصادر بيانات لهذه العملية.

أنت بحاجة إلى استخدام مناطق دمج البريد إذا كنت تريد توسيع الأجزاء ديناميكيًا داخل مستند . بدون مناطق دمج البريد، سيتم تكرار المستند بالكامل لكل سجل لمصدر البيانات.

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
    // 1 - استخدم الجدول بأكمله لدمج البريد لإنشاء مستند دمج بريدي واحد لكل صف في الجدول:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - استخدم صفًا واحدًا من الجدول لإنشاء مستند واحد لدمج البريد:
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


