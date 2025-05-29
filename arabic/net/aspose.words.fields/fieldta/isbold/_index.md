---
title: FieldTA.IsBold
linktitle: IsBold
articleTitle: IsBold
second_title: Aspose.Words لـ .NET
description: حسّن تجربتك مع FieldTA! تحكّم بسهولة بتنسيق الخط العريض لأرقام الصفحات المدخلة، مما يضمن الوضوح والتركيز في مستنداتك.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldta/isbold/
---
## FieldTA.IsBold property

يحصل على أو يحدد ما إذا كان سيتم تطبيق التنسيق الغامق على رقم الصفحة للإدخال.

```csharp
public bool IsBold { get; set; }
```

## أمثلة

يوضح كيفية إنشاء جدول السلطات وتخصيصه باستخدام حقول TOA وTA.

```csharp
public void FieldTOA()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // أدخل حقل TOA، والذي سيؤدي إلى إنشاء إدخال لكل حقل TA في المستند،
    // عرض الاستشهادات الطويلة وأرقام الصفحات لكل إدخال.
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // عيّن فئة الإدخال لجدولنا. سيتضمن هذا TOA الآن حقول TA فقط.
    // التي لها قيمة مطابقة في خاصية EntryCategory الخاصة بها.
    fieldToa.EntryCategory = "1";

    // علاوة على ذلك، فإن فئة جدول السلطات في الفهرس 1 هي "الحالات"،
    // والذي سيظهر كعنوان لجدولنا إذا قمنا بتعيين هذا المتغير إلى true.
    fieldToa.UseHeading = true;

    // يمكننا تصفية حقول TA بشكل أكبر عن طريق تسمية إشارة مرجعية يجب أن تكون ضمن حدود TOA.
    fieldToa.BookmarkName = "MyBookmark";

    // بشكل افتراضي، يظهر خط منقط على مستوى الصفحة بين الاستشهادات في حقل TA
    // ورقم الصفحة. يمكننا استبداله بأي نص نضعه على هذه الخاصية.
    // سيؤدي إدراج حرف علامة التبويب إلى الحفاظ على علامة التبويب الأصلية.
    fieldToa.EntrySeparator = " \t p.";

    // إذا كان لدينا إدخالات TA متعددة تشترك في نفس الاقتباس الطويل،
    // ستظهر جميع أرقام الصفحات الخاصة بهم في صف واحد.
    //يمكننا استخدام هذه الخاصية لتحديد سلسلة من شأنها فصل أرقام الصفحات.
    fieldToa.PageNumberListSeparator = " & p. ";

    // يمكننا ضبط هذا على "صحيح" لجعل جدولنا يعرض الكلمة "passim"
    // إذا كان هناك خمسة أرقام صفحات أو أكثر في صف واحد.
    fieldToa.UsePassim = true;

    // يمكن لحقل TA واحد أن يشير إلى مجموعة من الصفحات.
    //يمكننا تحديد سلسلة هنا لتظهر بين أرقام الصفحة الأولية والنهائية لمثل هذه النطاقات.
    fieldToa.PageRangeSeparator = " to ";

    //سيتم نقل التنسيق من حقول TA إلى جدولنا.
    //يمكننا تعطيل هذا عن طريق تعيين علم RemoveEntryFormatting.
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // لن يظهر حقل TA هذا كإدخال في TOA لأنه خارج
    // حدود الإشارة المرجعية التي تحددها خاصية BookmarkName الخاصة بـ TOA.
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    // هذا الحقل TA موجود داخل الإشارة المرجعية،
    // ولكن فئة الإدخال لا تتطابق مع فئة الجدول، لذا فإن حقل TA لن يتضمنها.
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    //سيظهر هذا الإدخال في الجدول.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // لا يعرض جدول TOA الاستشهادات القصيرة،
    // ولكن يمكننا استخدامها كاختصار للإشارة إلى أسماء المصادر الضخمة التي تشير إليها حقول TA المتعددة.
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    // يمكننا تنسيق رقم الصفحة لجعله غامقًا/مائلًا باستخدام الخصائص التالية.
    // سوف نستمر في رؤية هذه التأثيرات إذا قمنا بتعيين جدولنا لتجاهل التنسيق.
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    // يمكننا تكوين حقول TA للحصول على إدخالات TOA الخاصة بها للإشارة إلى مجموعة من الصفحات التي يمتد عبرها الإشارة المرجعية.
    // لاحظ أن هذا الإدخال يشير إلى نفس المصدر المذكور أعلاه لمشاركة صف واحد في جدولنا.
    // سيحتوي هذا الصف على رقم الصفحة للإدخال أعلاه ونطاق الصفحة لهذا الإدخال،
    // مع قائمة صفحات الجدول وفواصل نطاق أرقام الصفحات بين أرقام الصفحات.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");
    fieldTA.PageRangeBookmarkName = "MyMultiPageBookmark";

    builder.StartBookmark("MyMultiPageBookmark");
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.EndBookmark("MyMultiPageBookmark");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", fieldTA.GetFieldCode());

    // إذا قمنا بتمكين ميزة "Passim" في جدولنا، فإن وجود 5 أو أكثر من إدخالات TA بنفس المصدر سيؤدي إلى استدعائها.
    for (int i = 0; i < 5; i++)
    {
        InsertToaEntry(builder, "1", "Source 4");
    }

    builder.EndBookmark("MyBookmark");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOA.TA.docx");
}

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
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
