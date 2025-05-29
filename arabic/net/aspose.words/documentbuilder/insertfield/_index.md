---
title: DocumentBuilder.InsertField
linktitle: InsertField
articleTitle: InsertField
second_title: Aspose.Words لـ .NET
description: حسّن مستنداتك باستخدام طريقة InsertField من DocumentBuilder. أضف حقول Word وحدّثها بسهولة لتحسين المحتوى الديناميكي والوظائف.
type: docs
weight: 330
url: /ar/net/aspose.words/documentbuilder/insertfield/
---
## InsertField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool*) {#insertfield}

يقوم بإدراج حقل Word في مستند ويقوم بشكل اختياري بتحديث نتيجة الحقل.

```csharp
public Field InsertField(FieldType fieldType, bool updateField)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldType | FieldType | نوع الحقل المراد إضافته. |
| updateField | Boolean | يحدد ما إذا كان سيتم تحديث الحقل على الفور. |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field/) الكائن الذي يمثل الحقل المدرج.

## ملاحظات

تُدرج هذه الطريقة حقلاً في مستند. يمكن لـ Aspose.Words تحديث معظم أنواع الحقول، ولكن ليس جميعها. لمزيد من التفاصيل، راجع ملف x000d.`InsertField` التحميل الزائد.

## أمثلة

يوضح كيفية إدراج حقل في مستند باستخدام FieldType.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقلين أثناء تمرير علم يحدد ما إذا كان سيتم تحديثهما أثناء قيام المنشئ بإدراجهما.
// في بعض الحالات، قد يكون تحديث الحقول مكلفًا من الناحية الحسابية، وقد يكون من الجيد تأجيل التحديث.
doc.BuiltInDocumentProperties.Author = "John Doe";
builder.Write("This document was written by ");
builder.InsertField(FieldType.FieldAuthor, updateInsertedFieldsImmediately);

builder.InsertParagraph();
builder.Write("\nThis is page ");
builder.InsertField(FieldType.FieldPage, updateInsertedFieldsImmediately);

Assert.AreEqual(" AUTHOR ", doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(" PAGE ", doc.Range.Fields[1].GetFieldCode());

if (updateInsertedFieldsImmediately)
{
    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);
    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
else
{
    Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
    Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

    // سوف نحتاج إلى تحديث هذه الحقول باستخدام طرق التحديث يدويًا.
    doc.Range.Fields[0].Update();

    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);

    doc.UpdateFields();

    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
```

### أنظر أيضا

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertField(*string*) {#insertfield_1}

يقوم بإدراج حقل Word في مستند ويقوم بتحديث نتيجة الحقل.

```csharp
public Field InsertField(string fieldCode)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldCode | String | رمز الحقل المراد إدراجه (بدون أقواس متعرجة). |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field/) الكائن الذي يمثل الحقل المدرج.

## ملاحظات

تُدرج هذه الطريقة حقلاً في مستند وتُحدّث نتيجة الحقل فورًا. يُمكن لـ Aspose.Words تحديث معظم أنواع الحقول، ولكن ليس جميعها. لمزيد من التفاصيل، راجع `InsertField` التحميل الزائد.

## أمثلة

يوضح كيفية إدراج حقل في مستند باستخدام رمز الحقل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// يؤدي هذا التحميل الزائد لطريقة InsertField إلى تحديث الحقول المدرجة تلقائيًا.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

يوضح كيفية إدراج الحقول، ونقل مؤشر منشئ المستندات إليها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// نقل المؤشر إلى MERGEFIELD الأول.
builder.MoveToMergeField("MyMergeField1", true, false);

// لاحظ أن المؤشر يوضع مباشرة بعد MERGEFIELD الأول، وقبل الثاني.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// إذا أردنا تحرير كود الحقل أو محتوياته باستخدام المنشئ،
//يجب أن يكون المؤشر داخل حقل.
// لوضعه داخل حقل، سنحتاج إلى استدعاء طريقة MoveTo الخاصة بمنشئ المستندات
// ومرر عقدة بداية الحقل أو الفاصلة كحجة.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### أنظر أيضا

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertField(*string, string*) {#insertfield_2}

يقوم بإدراج حقل Word في مستند دون تحديث نتيجة الحقل.

```csharp
public Field InsertField(string fieldCode, string fieldValue)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldCode | String | رمز الحقل المراد إدراجه (بدون أقواس متعرجة). |
| fieldValue | String | قيمة الحقل المراد إدراجها. تمرير`باطل` للحقول التي لا تحتوي على قيمة. |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field/) الكائن الذي يمثل الحقل المدرج.

## ملاحظات

تتكون الحقول في مستندات مايكروسوفت وورد من رمز حقل ونتيجة حقل. يشبه رمز الحقل صيغة، وتكون النتيجة هي القيمة التي تنتجها الصيغة. قد يحتوي رمز الحقل أيضًا على مفاتيح حقل، وهي بمثابة تعليمات إضافية لتنفيذ إجراء محدد.

يمكنك التبديل بين عرض رموز الحقول والنتائج في مستندك في Microsoft Word باستخدام اختصار لوحة المفاتيح Alt+F9. تظهر رموز الحقول بين أقواس متعرجة ( { } ).

لإنشاء حقل، يجب عليك تحديد نوع الحقل ورمز الحقل وقيمة حقل "عنصر نائب". إذا لم تكن متأكدًا من صيغة رمز حقل معين، فقم بإنشاء الحقل في Microsoft Word first والتبديل لرؤية رمز الحقل الخاص به.

يمكن لـ Aspose.Words حساب نتائج الحقول لمعظم أنواع الحقول، ولكن هذه الطريقة لا تُحدّث نتيجة الحقل تلقائيًا. ولأن نتيجة الحقل لا تُحسب تلقائيًا، فمن المتوقع أن تُمرّر قيمة نصية (أو حتى سلسلة نصية فارغة) ليتم إدراجها في حقل النتيجة. ستبقى هذه القيمة في حقل النتيجة كعنصر نائب حتى يتم تحديث الحقل. لتحديث نتيجة الحقل، يمكنك استدعاء[`Update`](../../../aspose.words.fields/field/update/) في حقل الكائن الذي تم إرجاعه إليك أو[`UpdateFields`](../../document/updatefields/) لتحديث الحقول في المستند بأكمله.

## أمثلة

يوضح كيفية إعداد ترقيم الصفحات في قسم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 3.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("Section 2, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 3.");

// نقل منشئ المستند إلى العنوان الأساسي للقسم الأول،
// والتي سيتم عرضها في كل صفحة في هذا القسم.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// أدخل حقل PAGE، والذي سيعرض رقم الصفحة الحالية.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// قم بتكوين القسم بحيث يبدأ عدد الصفحات التي تعرضها حقول الصفحة من 5.
// قم أيضًا بتكوين جميع حقول الصفحة لعرض أرقام صفحاتها باستخدام الأرقام الرومانية الكبيرة.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// قم بإنشاء رأس أساسي آخر للقسم الثاني، مع حقل PAGE آخر.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// قم بتكوين القسم بحيث يبدأ عدد الصفحات التي تعرضها حقول الصفحة من 10.
// قم أيضًا بتكوين جميع حقول الصفحة لعرض أرقام صفحاتها باستخدام الأرقام العربية.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### أنظر أيضا

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
