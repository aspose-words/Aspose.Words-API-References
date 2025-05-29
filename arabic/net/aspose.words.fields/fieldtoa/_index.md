---
title: FieldToa Class
linktitle: FieldToa
articleTitle: FieldToa
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FieldToa لتنفيذ حقول TOA بسلاسة. حسّن معالجة مستنداتك بميزات فعّالة اليوم!
type: docs
weight: 2930
url: /ar/net/aspose.words.fields/fieldtoa/
---
## FieldToa class

ينفذ حقل TOA.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldToa : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldToa](fieldtoa/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldtoa/bookmarkname/) { get; set; } | يحصل على اسم الإشارة المرجعية التي تحدد الجزء من المستند المستخدم لبناء الجدول أو يعينه. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [EntryCategory](../../aspose.words.fields/fieldtoa/entrycategory/) { get; set; } | يحصل على الفئة المتكاملة للإدخالات المضمنة في الجدول أو يعينها. |
| [EntrySeparator](../../aspose.words.fields/fieldtoa/entryseparator/) { get; set; } | يحصل على أو يعين تسلسل الأحرف المستخدم لفصل إدخال جدول السلطات ورقم الصفحة الخاص به. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/)الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | يحصل على أو يحدد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | يحصل على أو يحدد ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب نتيجته). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | يحصل على أو يعين LCID للحقل. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldtoa/pagenumberlistseparator/) { get; set; } | يحصل على أو يعين تسلسل الأحرف المستخدم لفصل رقمين للصفحات في قائمة أرقام الصفحات. |
| [PageRangeSeparator](../../aspose.words.fields/fieldtoa/pagerangeseparator/) { get; set; } | يحصل على أو يعين تسلسل الأحرف المستخدم لفصل بداية ونهاية نطاق الصفحة. |
| [RemoveEntryFormatting](../../aspose.words.fields/fieldtoa/removeentryformatting/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم إزالة تنسيق نص الإدخال في المستند من الإدخال في جدول السلطات. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | يحصل على النص الموجود بين فاصل الحقل ونهاية الحقل أو يعينه. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن يكون`باطل` . |
| [SequenceName](../../aspose.words.fields/fieldtoa/sequencename/) { get; set; } | يحصل على اسم التسلسل الذي تم تضمين رقمه مع رقم الصفحة أو يعينه. |
| [SequenceSeparator](../../aspose.words.fields/fieldtoa/sequenceseparator/) { get; set; } | يحصل على أو يعين تسلسل الأحرف المستخدم لفصل أرقام التسلسل وأرقام الصفحات. |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | يحصل على نوع حقل Microsoft Word. |
| [UseHeading](../../aspose.words.fields/fieldtoa/useheading/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم تضمين عنوان الفئة للإدخالات في جدول السلطات. |
| [UsePassim](../../aspose.words.fields/fieldtoa/usepassim/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم استبدال خمسة أو أكثر من المراجع المختلفة للصفحات لنفس المرجع بـ "passim"، والذي يستخدم للإشارة إلى أن الكلمة أو المقطع يظهر بشكل متكرر في العمل المذكور. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | يُزيل الحقل من المستند. يُرجع عقدة بعد الحقل مباشرةً. إذا كانت نهاية الحقل هي آخر عقدة فرعية للعقدة الأصلية، تُرجع فقرته الأصلية. إذا كان الحقل قد حُذف مُسبقًا، تُرجع`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يُجري تحديث الحقل. يُطرح هذا الخطأ إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | يُجري تحديثًا للحقل. يُطرح هذا الخطأ إذا كان الحقل قيد التحديث بالفعل. |

## ملاحظات

يقوم ببناء جدول السلطات (أي قائمة المراجع في مستند قانوني، مثل المراجع للقضايا والتشريعات والقواعد، بالإضافة إلى أرقام الصفحات التي تظهر فيها المراجع) باستخدام إدخالات المحددة بواسطة حقول TA.

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

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
