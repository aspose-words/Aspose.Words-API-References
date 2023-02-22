---
title: FieldTA.PageRangeBookmarkName
second_title: Aspose.Words لمراجع .NET API
description: FieldTA ملكية. الحصول على أو تعيين اسم الإشارة المرجعية التي تحدد نطاقًا من الصفحات المدرجة كرقم صفحة الإدخال.
type: docs
weight: 60
url: /ar/net/aspose.words.fields/fieldta/pagerangebookmarkname/
---
## FieldTA.PageRangeBookmarkName property

الحصول على أو تعيين اسم الإشارة المرجعية التي تحدد نطاقًا من الصفحات المدرجة كرقم صفحة الإدخال.

```csharp
public string PageRangeBookmarkName { get; set; }
```

### أمثلة

يُظهر كيفية إنشاء جدول مصادر وتخصيصه باستخدام حقلي TOA و TA.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // أدخل حقل TOA ، والذي سينشئ إدخالًا لكل حقل TA في المستند ،
    // عرض الاستشهادات الطويلة وأرقام الصفحات لكل إدخال.
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // تعيين فئة الدخول لجدولنا. ستشمل TOA الآن حقول TA فقط
    // التي لها قيمة مطابقة في خاصية EntryCategory الخاصة بها.
    fieldToa.EntryCategory = "1";

    // علاوة على ذلك ، فإن فئة جدول المراجع في الفهرس 1 هي "القضايا" ،
    // والذي سيظهر كعنوان لجدولنا إذا قمنا بتعيين هذا المتغير على صحيح.
    fieldToa.UseHeading = true;

    // يمكننا كذلك تصفية حقول TA عن طريق تسمية إشارة مرجعية يجب أن تكون ضمن حدود TOA.
    fieldToa.BookmarkName = "MyBookmark";

    // بشكل افتراضي ، تظهر علامة تبويب على مستوى الصفحة ذات سطر منقط بين اقتباس حقل TA
    // ورقم صفحتها. يمكننا استبداله بأي نص نضعه على هذه الخاصية.
    // سيؤدي إدراج حرف جدولة إلى الاحتفاظ بعلامة التبويب الأصلية.
    fieldToa.EntrySeparator = " \t p.";

    // إذا كان لدينا العديد من إدخالات TA التي تشترك في نفس الاقتباس الطويل ،
    // ستظهر جميع أرقام الصفحات الخاصة بهم في صف واحد.
    // يمكننا استخدام هذه الخاصية لتحديد سلسلة تفصل أرقام صفحاتهم.
    fieldToa.PageNumberListSeparator = " & p. ";

    // يمكننا ضبط هذا على "صحيح" لجعل طاولتنا تعرض كلمة "passim"
    // إذا كان هناك خمسة أو أكثر من أرقام الصفحات في صف واحد.
    fieldToa.UsePassim = true;

    // يمكن أن يشير حقل TA إلى مجموعة من الصفحات.
    // يمكننا تحديد سلسلة هنا لتظهر بين أرقام صفحات البداية والنهاية لمثل هذه النطاقات.
    fieldToa.PageRangeSeparator = " to ";

    // سينتقل التنسيق من حقول TA إلى جدولنا.
    // يمكننا تعطيل هذا عن طريق تعيين علامة RemoveEntryFormatting.
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // لن يظهر حقل TA هذا كإدخال في TOA لأنه خارج
    // حدود الإشارة المرجعية التي تحددها خاصية BookmarkName TOA.
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    // يوجد حقل TA هذا داخل الإشارة المرجعية ،
    // لكن فئة الإدخال لا تتطابق مع فئة الجدول ، لذلك لن يتضمنها حقل TA.
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    // سيظهر هذا الإدخال في الجدول.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // لا يعرض جدول TOA اقتباسات قصيرة ،
    // ولكن يمكننا استخدامها كاختصار للإشارة إلى أسماء المصادر الضخمة التي تشير إليها حقول TA المتعددة.
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    // يمكننا تنسيق رقم الصفحة لجعلها غامقة / مائلة باستخدام الخصائص التالية.
    // سنظل نرى هذه التأثيرات إذا وضعنا جدولنا لتجاهل التنسيق.
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    // يمكننا تكوين حقول TA للحصول على مدخلات TOA الخاصة بهم للإشارة إلى مجموعة من الصفحات التي تمتد عبرها إشارة مرجعية.
    // لاحظ أن هذا الإدخال يشير إلى نفس المصدر المذكور أعلاه لمشاركة صف واحد في جدولنا.
    // سيحتوي هذا الصف على رقم صفحة الإدخال أعلاه ونطاق صفحات هذا الإدخال ،
    // مع قائمة صفحات الجدول وفواصل نطاق رقم الصفحة بين أرقام الصفحات.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");
    fieldTA.PageRangeBookmarkName = "MyMultiPageBookmark";

    builder.StartBookmark("MyMultiPageBookmark");
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.EndBookmark("MyMultiPageBookmark");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", fieldTA.GetFieldCode());

    // إذا قمنا بتمكين ميزة "Passim" في طاولتنا ، فإن وجود 5 أو أكثر من إدخالات TA مع نفس المصدر سوف يستدعيها.
    for (int i = 0; i < 5; i++)
    {
        InsertToaEntry(builder, "1", "Source 4");
    }

    builder.EndBookmark("MyBookmark");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOA.TA.docx");

private static FieldTA InsertToaEntry(DocumentBuilder builder, string entryCategory, string longCitation)
{
    FieldTA field = (FieldTA)builder.InsertField(FieldType.FieldTOAEntry, false);
    field.EntryCategory = entryCategory;
    field.LongCitation = longCitation;

    builder.InsertBreak(BreakType.PageBreak);

    return field;
}
```

### أنظر أيضا

* class [FieldTA](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldta/)
* المجسم [Aspose.Words](../../../)


