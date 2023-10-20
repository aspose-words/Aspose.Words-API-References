---
title: FieldEQ Class
linktitle: FieldEQ
articleTitle: FieldEQ
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fields.FieldEQ فصل. ينفذ حقل EQ في C#.
type: docs
weight: 1830
url: /ar/net/aspose.words.fields/fieldeq/
---
## FieldEQ class

ينفذ حقل EQ.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldEQ : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldEQ](fieldeq/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | الحصول على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/) الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تعيين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | الحصول على أو تعيين ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تعيين LCID الخاص بالحقل. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقول. يمكن ان يكون`باطل` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | الحصول على نوع حقل Microsoft Word. |

## طُرق

| اسم | وصف |
| --- | --- |
| [AsOfficeMath](../../aspose.words.fields/fieldeq/asofficemath/)() | إرجاع كائن Office Math المتوافق مع حقل EQ. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | إزالة الحقل من المستند. إرجاع عقدة مباشرة بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير للعقدة الأصلية، فسيتم إرجاع الفقرة الأصلية الخاصة به. إذا تمت إزالة الحقل بالفعل، فسيتم إرجاعه`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يقوم بإجراء التحديث الميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | إجراء تحديث ميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |

## أمثلة

يوضح كيفية استبدال حقل EQ بـ Office Math.

```csharp
Document doc = new Document(MyDir + "Field sample - EQ.docx");
FieldEQ fieldEQ = doc.Range.Fields.OfType<FieldEQ>().First();

OfficeMath officeMath = fieldEQ.AsOfficeMath();

fieldEQ.Start.ParentNode.InsertBefore(officeMath, fieldEQ.Start);
fieldEQ.Remove();

doc.Save(ArtifactsDir + "Field.EQAsOfficeMath.docx");
```

يوضح كيفية استخدام حقل EQ لعرض مجموعة متنوعة من المعادلات الرياضية.

```csharp
public void FieldEQ()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // يعرض حقل EQ معادلة رياضية تتكون من عنصر واحد أو عدة عناصر.
    // يأخذ كل عنصر الشكل التالي: [التبديل] [الخيارات] [الوسائط].
    // قد يكون هناك مفتاح واحد والعديد من الخيارات الممكنة.
    // الوسائط عبارة عن مجموعة من القيم المفصولة بفاصلة ومحاطة بأقواس مستديرة.

    // نستخدم هنا أداة إنشاء المستندات لإدراج حقل EQ، باستخدام المفتاح "\f"، الذي يتوافق مع "الكسر".
    // سنمرر القيمتين 1 و4 كوسائط، ولن نستخدم أي خيارات.
    // سيعرض هذا الحقل كسرًا يكون بسطه 1 ومقامه 4.
    FieldEQ field = InsertFieldEQ(builder, @"\f(1,4)");

    Assert.AreEqual(@" EQ \f(1,4)", field.GetFieldCode());

    // قد يحتوي حقل EQ واحد على عناصر متعددة موضوعة بشكل تسلسلي.
    // يمكننا أيضًا دمج العناصر داخل بعضها البعض عن طريق وضع العناصر الداخلية
    // داخل أقواس الوسيطة للعناصر الخارجية.
    // يمكننا العثور على القائمة الكاملة للمفاتيح مع استخداماتها هنا:
    // https://blogs.msdn.microsoft.com/murrays/2018/01/23/microsoft-word-eq-field/

     // يوجد أدناه تطبيقات لتسعة مفاتيح مختلفة لمجال EQ يمكننا استخدامها لإنشاء أنواع مختلفة من الكائنات.
    // 1 - مفتاح المصفوفة "\a"، بمحاذاة لليسار، عمودين، 3 نقاط من التباعد الأفقي والرأسي:
    InsertFieldEQ(builder, @"\a \al \co2 \vs3 \hs3(4x,- 4y,-4x,+ y)");

    // 2 - مفتاح القوس "\b"، حرف القوس "["، لإحاطة المحتويات بمجموعة من الأقواس المربعة:
    // لاحظ أننا نقوم بتداخل مصفوفة داخل الأقواس، والتي ستبدو تمامًا كمصفوفة في المخرجات.
    InsertFieldEQ(builder, @"\b \bc\[ (\a \al \co3 \vs3 \hs3(1,0,0,0,1,0,0,0,1))");

    // 3 - مفتاح الإزاحة "\d"، لإزاحة النص "B" بمقدار 30 مسافة إلى يمين "A"، مع عرض الفجوة كتسطير:
    InsertFieldEQ(builder, @"A \d \fo30 \li() B");

    // 4 - صيغة تتكون من كسور متعددة:
    InsertFieldEQ(builder, @"\f(d,dx)(u + v) = \f(du,dx) + \f(dv,dx)");

    // 5 - التبديل التكاملي "\i"، مع رمز الجمع:
    InsertFieldEQ(builder, @"\i \su(n=1,5,n)");

    // 6 - تبديل القائمة "\l":
    InsertFieldEQ(builder, @"\l(1,1,2,3,n,8,13)");

    // 7 - المفتاح الجذري "\r"، يعرض الجذر التكعيبي لـ x:
    InsertFieldEQ(builder, @"\r (3,x)");

    // 8 - تبديل الحرف المنخفض/المرتفع "/s"، أولاً كحرف مرتفع ثم كحرف منخفض:
    InsertFieldEQ(builder, @"\s \up8(Superscript) Text \s \do8(Subscript)");

    // 9 - مربع التبديل "\x"، مع وجود خطوط في أعلى وأسفل ويسار ويمين الإدخال:
    InsertFieldEQ(builder, @"\x \to \bo \le \ri(5)");

    // بعض المجموعات الأكثر تعقيدًا.
    InsertFieldEQ(builder, @"\a \ac \vs1 \co1(lim,n→∞) \b (\f(n,n2 + 12) + \f(n,n2 + 22) + ... + \f(n,n2 + n2))");
    InsertFieldEQ(builder, @"\i (,,  \b(\f(x,x2 + 3x + 2))) \s \up10(2)");
    InsertFieldEQ(builder, @"\i \in( tan x, \s \up2(sec x), \b(\r(3) )\s \up4(t) \s \up7(2)  dt)");

    doc.Save(ArtifactsDir + "Field.EQ.docx");
}

/// <summary>
/// استخدم أداة إنشاء المستندات لإدراج حقل EQ وتعيين وسائطه وبدء فقرة جديدة.
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

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
