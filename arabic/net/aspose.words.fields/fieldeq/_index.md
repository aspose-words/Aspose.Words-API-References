---
title: FieldEQ Class
linktitle: FieldEQ
articleTitle: FieldEQ
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FieldEQ لتطبيق حقول EQ بسلاسة. عزّز أتمتة المستندات بميزات فعّالة ومرونة عالية.
type: docs
weight: 2240
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
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/)الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | يحصل على أو يحدد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | يحصل على أو يحدد ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب نتيجته). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | يحصل على أو يعين LCID للحقل. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | يحصل على النص الموجود بين فاصل الحقل ونهاية الحقل أو يعينه. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن يكون`باطل` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | يحصل على نوع حقل Microsoft Word. |

## طُرق

| اسم | وصف |
| --- | --- |
| [AsOfficeMath](../../aspose.words.fields/fieldeq/asofficemath/)() | إرجاع كائن Office Math الذي يتوافق مع حقل EQ. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | يُزيل الحقل من المستند. يُرجع عقدة بعد الحقل مباشرةً. إذا كانت نهاية الحقل هي آخر عقدة فرعية للعقدة الأصلية، تُرجع فقرته الأصلية. إذا كان الحقل قد حُذف مُسبقًا، تُرجع`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يُجري تحديث الحقل. يُطرح هذا الخطأ إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | يُجري تحديثًا للحقل. يُطرح هذا الخطأ إذا كان الحقل قيد التحديث بالفعل. |

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

    // يعرض حقل EQ معادلة رياضية تتكون من عنصر واحد أو عناصر متعددة.
    // يأخذ كل عنصر الشكل التالي: [التبديل][الخيارات][الحجج].
    //قد يكون هناك مفتاح واحد، والعديد من الخيارات الممكنة.
    //الحجج عبارة عن مجموعة من القيم المنفصلة بفاصلة محاطة بأقواس دائرية.

    // هنا نستخدم منشئ المستندات لإدراج حقل EQ، مع مفتاح "\f"، والذي يتوافق مع "Fraction".
    // سوف نقوم بتمرير القيمتين 1 و 4 كحجج، ولن نستخدم أي خيارات.
    // سيعرض هذا الحقل كسرًا يتكون من 1 كبسط و4 كمقام.
    FieldEQ field = InsertFieldEQ(builder, @"\f(1,4)");

    Assert.AreEqual(@" EQ \f(1,4)", field.GetFieldCode());

    // قد يحتوي حقل EQ واحد على عناصر متعددة موضوعة بشكل تسلسلي.
    // يمكننا أيضًا تعشيش العناصر داخل بعضها البعض عن طريق وضع العناصر الداخلية
    // داخل أقواس الوسيطة للعناصر الخارجية.
    // يمكننا العثور على القائمة الكاملة للمفاتيح، إلى جانب استخداماتها هنا:
    // https://blogs.msdn.microsoft.com/murrays/2018/01/23/microsoft-word-eq-field/

     // فيما يلي تطبيقات لتسعة مفاتيح مجال EQ مختلفة يمكننا استخدامها لإنشاء أنواع مختلفة من الكائنات.
    // 1 - مفتاح المصفوفة "\a"، محاذي لليسار، عمودان، 3 نقاط من التباعد الأفقي والرأسي:
    InsertFieldEQ(builder, @"\a \al \co2 \vs3 \hs3(4x,- 4y,-4x,+ y)");

    // 2 - مفتاح الأقواس "\b"، حرف الأقواس "["، لإحاطة المحتويات بمجموعة من الأقواس المربعة:
    // لاحظ أننا نقوم بتضمين مصفوفة داخل الأقواس، والتي ستبدو في المجمل مثل مصفوفة في الإخراج.
    InsertFieldEQ(builder, @"\b \bc\[ (\a \al \co3 \vs3 \hs3(1,0,0,0,1,0,0,0,1))");

    // 3 - مفتاح الإزاحة "\d"، إزاحة النص "B" 30 مسافة إلى يمين "A"، وعرض الفجوة على شكل خط سفلي:
    InsertFieldEQ(builder, @"A \d \fo30 \li() B");

    // 4 - صيغة مكونة من كسور متعددة:
    InsertFieldEQ(builder, @"\f(d,dx)(u + v) = \f(du,dx) + \f(dv,dx)");

    // 5 - مفتاح تكاملي "\i"، مع رمز الجمع:
    InsertFieldEQ(builder, @"\i \su(n=1,5,n)");

    // 6 - تبديل القائمة "\l":
    InsertFieldEQ(builder, @"\l(1,1,2,3,n,8,13)");

    // 7 - مفتاح جذري "\r"، يعرض الجذر التكعيبي لـ x:
    InsertFieldEQ(builder, @"\r (3,x)");

    // 8 - التبديل بين الحرف السفلي والحرف العلوي "/s"، أولاً كحرف علوي ثم كحرف سفلي:
    InsertFieldEQ(builder, @"\s \up8(Superscript) Text \s \do8(Subscript)");

    // 9 - مفتاح الصندوق "\x"، مع خطوط في الأعلى والأسفل واليسار واليمين من المدخل:
    InsertFieldEQ(builder, @"\x \to \bo \le \ri(5)");

    // بعض التركيبات الأكثر تعقيدًا.
    InsertFieldEQ(builder, @"\a \ac \vs1 \co1(lim,n→∞) \b (\f(n,n2 + 12) + \f(n,n2 + 22) + ... + \f(n,n2 + n2))");
    InsertFieldEQ(builder, @"\i (,,  \b(\f(x,x2 + 3x + 2))) \s \up10(2)");
    InsertFieldEQ(builder, @"\i \in( tan x, \s \up2(sec x), \b(\r(3) )\s \up4(t) \s \up7(2)  dt)");

    doc.Save(ArtifactsDir + "Field.EQ.docx");
}

/// <summary>
/// استخدم منشئ المستندات لإدراج حقل EQ وتعيين وسيطاته وبدء فقرة جديدة.
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
