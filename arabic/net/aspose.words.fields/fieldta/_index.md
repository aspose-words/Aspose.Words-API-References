---
title: FieldTA Class
linktitle: FieldTA
articleTitle: FieldTA
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fields.FieldTA فصل. ينفذ حقل TA في C#.
type: docs
weight: 2470
url: /ar/net/aspose.words.fields/fieldta/
---
## FieldTA class

ينفذ حقل TA.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldTA : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldTA](fieldta/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | الحصول على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [EntryCategory](../../aspose.words.fields/fieldta/entrycategory/) { get; set; } | الحصول على أو تعيين فئة الإدخال المتكامل، وهو رقم يتوافق مع ترتيب الفئات. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/) الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IsBold](../../aspose.words.fields/fieldta/isbold/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم تطبيق التنسيق الغامق على رقم الصفحة للإدخال. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تعيين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى تم إجراؤها على المستند. |
| [IsItalic](../../aspose.words.fields/fieldta/isitalic/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم تطبيق التنسيق المائل على رقم الصفحة للإدخال. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | الحصول على أو تعيين ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تعيين LCID الخاص بالحقل. |
| [LongCitation](../../aspose.words.fields/fieldta/longcitation/) { get; set; } | الحصول على الاقتباس الطويل للإدخال أو تعيينه. |
| [PageRangeBookmarkName](../../aspose.words.fields/fieldta/pagerangebookmarkname/) { get; set; } | الحصول على أو تعيين اسم الإشارة المرجعية التي تحدد نطاقًا من الصفحات التي تم إدراجها كرقم صفحة الإدخال. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقول. يمكن ان يكون`باطل` . |
| [ShortCitation](../../aspose.words.fields/fieldta/shortcitation/) { get; set; } | الحصول على الاقتباس القصير للإدخال أو تعيينه. |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | الحصول على نوع حقل Microsoft Word. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | إزالة الحقل من المستند. إرجاع عقدة مباشرة بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير للعقدة الأصلية، فسيتم إرجاع الفقرة الأصلية الخاصة به. إذا تمت إزالة الحقل بالفعل، فسيتم إرجاعه`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يقوم بإجراء التحديث الميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | إجراء تحديث ميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |

## ملاحظات

يحدد النص ورقم الصفحة لجدول إدخال الاستنادات، والذي يستخدم بواسطة حقل TOA.

## أمثلة

يوضح كيفية إنشاء جدول المراجع المصدقة وتخصيصه باستخدام حقلي TOA وTA.

```csharp
public void FieldTOA()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // أدخل حقل TOA، والذي سيؤدي إلى إنشاء إدخال لكل حقل TA في المستند،
    // عرض الاستشهادات الطويلة وأرقام الصفحات لكل إدخال.
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // قم بتعيين فئة الإدخال لجدولنا. سيتضمن TOA الآن حقول TA فقط
    // التي لها قيمة مطابقة في خاصية EntryCategory الخاصة بها.
    fieldToa.EntryCategory = "1";

    // علاوة على ذلك، فإن جدول فئة السلطات في الفهرس 1 هو "القضايا"،
    // والذي سيظهر كعنوان لجدولنا إذا قمنا بتعيين هذا المتغير على صحيح.
    fieldToa.UseHeading = true;

    // يمكننا أيضًا تصفية حقول TA عن طريق تسمية إشارة مرجعية يجب أن تكون ضمن حدود TOA.
    fieldToa.BookmarkName = "MyBookmark";

    // بشكل افتراضي، تظهر علامة تبويب على مستوى الصفحة بخط منقط بين اقتباس حقل TA
    // ورقم صفحته. يمكننا استبداله بأي نص نضعه على هذه الخاصية.
    // سيؤدي إدراج حرف علامة التبويب إلى الحفاظ على علامة التبويب الأصلية.
    fieldToa.EntrySeparator = " \t p.";

    // إذا كان لدينا العديد من إدخالات TA التي تشترك في نفس الاقتباس الطويل،
    // ستظهر جميع أرقام الصفحات الخاصة بها في صف واحد.
    // يمكننا استخدام هذه الخاصية لتحديد سلسلة تفصل بين أرقام صفحاتها.
    fieldToa.PageNumberListSeparator = " & p. ";

    // يمكننا ضبط هذا على "صحيح" حتى يعرض جدولنا كلمة "passim"
    // إذا كان هناك خمسة أرقام صفحات أو أكثر في صف واحد.
    fieldToa.UsePassim = true;

    // يمكن أن يشير حقل TA واحد إلى مجموعة من الصفحات.
    // يمكننا تحديد سلسلة هنا لتظهر بين أرقام صفحة البداية والنهاية لمثل هذه النطاقات.
    fieldToa.PageRangeSeparator = " to ";

    // سيتم نقل التنسيق من حقول TA إلى جدولنا.
    // يمكننا تعطيل هذا عن طريق تعيين علامة RemoveEntryFormatting.
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // لن يظهر حقل TA هذا كمدخل في TOA لأنه موجود بالخارج
    // حدود الإشارة المرجعية التي تحددها خاصية BookmarkName الخاصة بـ TOA.
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    // حقل TA هذا موجود داخل الإشارة المرجعية،
    // لكن فئة الإدخال لا تتطابق مع فئة الجدول، لذلك لن يتضمنها حقل TA.
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    // سيظهر هذا الإدخال في الجدول.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // لا يعرض جدول TOA الاستشهادات القصيرة،
    // ولكن يمكننا استخدامها كاختصار للإشارة إلى أسماء المصادر الضخمة التي تشير إليها حقول TA المتعددة.
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    // يمكننا تنسيق رقم الصفحة لجعله غامقًا/مائلًا باستخدام الخصائص التالية.
    // سنظل نرى هذه التأثيرات إذا قمنا بتعيين جدولنا لتجاهل التنسيق.
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    // يمكننا تكوين حقول TA للحصول على إدخالات TOA الخاصة بها للإشارة إلى نطاق من الصفحات التي تمتد عبرها الإشارة المرجعية.
    // لاحظ أن هذا الإدخال يشير إلى نفس المصدر الموجود أعلاه لمشاركة صف واحد في جدولنا.
    // سيحتوي هذا الصف على رقم صفحة الإدخال أعلاه ونطاق صفحات هذا الإدخال،
    // مع قائمة صفحات الجدول وفواصل نطاق أرقام الصفحات بين أرقام الصفحات.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");
    fieldTA.PageRangeBookmarkName = "MyMultiPageBookmark";

    builder.StartBookmark("MyMultiPageBookmark");
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.EndBookmark("MyMultiPageBookmark");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", fieldTA.GetFieldCode());

    // إذا قمنا بتمكين ميزة "Passim" في جدولنا، فإن وجود 5 إدخالات TA أو أكثر من نفس المصدر سيؤدي إلى استدعائها.
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

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
