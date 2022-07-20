---
title: FieldEQ
second_title: Aspose.Words لمراجع .NET API
description: ينفذ حقل EQ .
type: docs
weight: 1680
url: /ar/net/aspose.words.fields/fieldeq/
---
## FieldEQ class

ينفذ حقل EQ .

```csharp
public class FieldEQ : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldEQ](fieldeq)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format) { get; } | يحصل على أ[`FieldFormat`](../fieldformat) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | الحصول على أو تحديد LCID للحقل. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | يحصل على العقدة التي تمثل فاصل المجال. يمكن أن يكون فارغًا. |
| [Start](../../aspose.words.fields/field/start) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | يحصل على نوع حقل Microsoft Word . |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . |
| [Remove](../../aspose.words.fields/field/remove)() | يزيل الحقل من المستند. إرجاع عقدة بعد الحقل مباشرة. إذا كانت نهاية الحقل هي آخر child من العقدة الأصلية ، يتم إرجاع فقرته الأصلية. إذا تمت إزالة الحقل بالفعل ، يعود **لا شيء** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update)() | يقوم بالتحديث الميداني. يرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update)(bool) | يقوم بإجراء تحديث ميداني. يرمي إذا تم تحديث الحقل بالفعل. |

### أمثلة

يوضح كيفية استخدام حقل EQ لعرض مجموعة متنوعة من المعادلات الرياضية.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // يعرض حقل EQ معادلة رياضية تتكون من عنصر واحد أو أكثر.
    // يأخذ كل عنصر الشكل التالي: [تبديل] [خيارات] [وسيطات].
    // قد يكون هناك مفتاح واحد والعديد من الخيارات الممكنة.
    // الوسيطات عبارة عن مجموعة من القيم المفصولة بغيبوبة محاطة بأقواس مستديرة.

    // هنا نستخدم منشئ المستندات لإدخال حقل EQ ، مع مفتاح تبديل "\ f" ، والذي يتوافق مع "كسر".
    // سنمرر القيمتين 1 و 4 كوسيطتين ، ولن نستخدم أي خيارات.
    // سيعرض هذا الحقل كسرًا بحيث يكون 1 هو البسط و 4 هو المقام.
    FieldEQ field = InsertFieldEQ(builder, @"\f(1,4)");

    Assert.AreEqual(@" EQ \f(1,4)", field.GetFieldCode());

    // قد يحتوي حقل EQ على عدة عناصر موضوعة بالتسلسل.
    // يمكننا أيضًا تداخل العناصر داخل بعضها البعض عن طريق وضع العناصر الداخلية
    // داخل أقواس الوسيطة للعناصر الخارجية.
    // يمكننا العثور على القائمة الكاملة للمفاتيح ، جنبًا إلى جنب مع استخداماتها هنا:
    // https://blogs.msdn.microsoft.com/murrays/2018/01/23/microsoft-word-eq-field/

    // فيما يلي تطبيقات تسعة مفاتيح مختلفة لمجال EQ يمكننا استخدامها لإنشاء أنواع مختلفة من الكائنات.
    // 1 - تبديل الصفيف "\ a" ، بمحاذاة إلى اليسار ، عمودين ، 3 نقاط من التباعد الأفقي والعمودي:
    InsertFieldEQ(builder, @"\a \al \co2 \vs3 \hs3(4x,- 4y,-4x,+ y)");

    // 2 - مفتاح القوس "\ b" ، حرف القوس "[" ، لإحاطة المحتويات بمجموعة من الأقواس المربعة:
    // لاحظ أننا نقوم بتداخل مصفوفة داخل الأقواس ، والتي ستبدو تمامًا مثل المصفوفة في الإخراج.
    InsertFieldEQ(builder, @"\b \bc\[ (\a \al \co3 \vs3 \hs3(1,0,0,0,1,0,0,0,1))");

    // 3 - مفتاح الإزاحة "\ d" ، مع إزاحة النص "ب" 30 مسافة إلى يمين "أ" ، مع عرض الفجوة كتسطير:
    InsertFieldEQ(builder, @"A \d \fo30 \li() B");

    // 4 - الصيغة المكونة من كسور متعددة:
    InsertFieldEQ(builder, @"\f(d,dx)(u + v) = \f(du,dx) + \f(dv,dx)");

    // 5 - مفتاح متكامل "\ i" ، برمز تجميع:
    InsertFieldEQ(builder, @"\i \su(n=1,5,n)");

    // 6 - مفتاح القائمة "\ l":
    InsertFieldEQ(builder, @"\l(1,1,2,3,n,8,13)");

    // 7 - تبديل جذري "\ r" ، يعرض جذرًا مكعّبًا لـ x:
    InsertFieldEQ(builder, @"\r (3,x)");

    // 8 - رمز التبديل "/ s" منخفض / مرتفع ، أولاً كحرف مرتفع ثم كمفتاح منخفض:
    InsertFieldEQ(builder, @"\s \up8(Superscript) Text \s \do8(Subscript)");

    // 9 - مربع التبديل "\ x" ، مع وجود خطوط أعلى الإدخال وأسفله ويساره ويمينه:
    InsertFieldEQ(builder, @"\x \to \bo \le \ri(5)");

    // بعض التركيبات الأكثر تعقيدًا.
    InsertFieldEQ(builder, @"\a \ac \vs1 \co1(lim,n→∞) \b (\f(n,n2 + 12) + \f(n,n2 + 22) + ... + \f(n,n2 + n2))");
    InsertFieldEQ(builder, @"\i (,,  \b(\f(x,x2 + 3x + 2))) \s \up10(2)");
    InsertFieldEQ(builder, @"\i \in( tan x, \s \up2(sec x), \b(\r(3) )\s \up4(t) \s \up7(2)  dt)");

    doc.Save(ArtifactsDir + "Field.EQ.docx");

/// <summary>
/// استخدم أداة إنشاء المستندات لإدراج حقل EQ ، واضبط وسيطاته وابدأ فقرة جديدة.
/// </summary>
private static FieldEQ InsertFieldEQ(DocumentBuilder builder, string args)
{
    FieldEQ field = (FieldEQ)builder.InsertField(FieldType.FieldEquation, true);
    builder.MoveTo(field.Separator);
    builder.Write(args);
    builder.MoveTo(field.Start.ParentNode);

    builder.InsertParagraph();
    return field;
}
```

### أنظر أيضا

* class [Field](../field)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
