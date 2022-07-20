---
title: InsertField
second_title: Aspose.Words لمراجع .NET API
description: إدراج حقل Word في مستند وتحديث نتيجة الحقل اختياريًا.
type: docs
weight: 300
url: /ar/net/aspose.words/documentbuilder/insertfield/
---
## InsertField(FieldType, bool) {#insertfield}

إدراج حقل Word في مستند وتحديث نتيجة الحقل اختياريًا.

```csharp
public Field InsertField(FieldType fieldType, bool updateField)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldType | FieldType | نوع الحقل المطلوب إلحاقه. |
| updateField | Boolean | يحدد ما إذا كان سيتم تحديث الحقل على الفور. |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field) كائن يمثل الحقل المدرج.

### ملاحظات

تقوم هذه الطريقة بإدراج حقل في المستند. لمزيد من التفاصيل راجع the [`InsertField`](../insertfield) الزائد.

### أمثلة

يوضح كيفية إدراج حقل في مستند باستخدام نوع الحقل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقلين أثناء تمرير علامة تحدد ما إذا كان سيتم تحديثهما أثناء قيام المنشئ بإدخالهما.
// في بعض الحالات ، قد يكون تحديث الحقول مكلفًا من الناحية الحسابية ، وقد يكون تأجيل التحديث فكرة جيدة.
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

    // سنحتاج إلى تحديث هذه الحقول باستخدام طرق التحديث يدويًا.
    doc.Range.Fields[0].Update();

    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);

    doc.UpdateFields();

    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
```

### أنظر أيضا

* class [Field](../../../aspose.words.fields/field)
* enum [FieldType](../../../aspose.words.fields/fieldtype)
* class [DocumentBuilder](../../documentbuilder)
* مساحة الاسم [Aspose.Words](../../documentbuilder)
* المجسم [Aspose.Words](../../../)

---

## InsertField(string) {#insertfield_1}

إدراج حقل Word في مستند وتحديث نتيجة الحقل.

```csharp
public Field InsertField(string fieldCode)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldCode | String | رمز الحقل المطلوب إدراجه (بدون الأقواس المتعرجة). |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field) كائن يمثل الحقل المدرج.

### ملاحظات

تُدخل هذه الطريقة حقلاً في المستند وتقوم بتحديث نتيجة الحقل على الفور. لمزيد من التفاصيل راجع the [`InsertField`](../insertfield) الزائد.

### أمثلة

يوضح كيفية إدراج حقل في مستند باستخدام رمز حقل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// هذا التحميل الزائد لطريقة InsertField يقوم تلقائيًا بتحديث الحقول المدرجة.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

يوضح كيفية إدراج الحقول ، وتحريك مؤشر منشئ المستندات إليها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// حرك المؤشر إلى MERGEFIELD الأول.
builder.MoveToMergeField("MyMergeField1", true, false);

// لاحظ أن المؤشر يتم وضعه مباشرة بعد MERGEFIELD الأول وقبل الثاني.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// إذا كنا نرغب في تحرير رمز الحقل أو المحتويات باستخدام المنشئ ،
// يجب أن يكون مؤشرها داخل حقل.
// لوضعه داخل حقل ، سنحتاج إلى استدعاء طريقة MoveTo لمنشئ المستندات
// وتمرير بداية الحقل أو العقدة الفاصلة كوسيطة.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### أنظر أيضا

* class [Field](../../../aspose.words.fields/field)
* class [DocumentBuilder](../../documentbuilder)
* مساحة الاسم [Aspose.Words](../../documentbuilder)
* المجسم [Aspose.Words](../../../)

---

## InsertField(string, string) {#insertfield_2}

إدراج حقل Word في مستند بدون تحديث نتيجة الحقل.

```csharp
public Field InsertField(string fieldCode, string fieldValue)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldCode | String | رمز الحقل المطلوب إدراجه (بدون الأقواس المتعرجة). |
| fieldValue | String | قيمة الحقل المطلوب إدراجها. تمرير فارغ للحقول التي ليس لها قيمة. |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field) كائن يمثل الحقل المدرج.

### ملاحظات

تتكون الحقول في مستندات Microsoft Word من رمز حقل ونتيجة حقل . رمز الحقل يشبه الصيغة وتكون نتيجة الحقل مثل القيمة التي تنتجها الصيغة. قد يحتوي رمز الحقل أيضًا على مفاتيح تبديل التي تشبه إرشادات إضافية لتنفيذ إجراء معين.

يمكنك التبديل بين عرض رموز الحقول والنتائج في المستند الخاص بك في Microsoft Word باستخدام اختصار لوحة المفاتيح Alt + F9. تظهر رموز الحقول بين الأقواس المتعرجة ({}).

لإنشاء حقل ، تحتاج إلى تحديد نوع الحقل ورمز الحقل وقيمة الحقل "عنصر نائب" ._ x000d_ إذا لم تكن متأكدًا من بناء جملة رمز حقل معين ، فأنشئ الحقل في Microsoft Word first وقم بالتبديل لرؤية رمز الحقل الخاص به .

Aspose.word يمكن للكلمات حساب نتائج الحقول لمعظم أنواع الحقول ، لكن هذه الطريقة لا تقوم بتحديث نتيجة الحقل تلقائيًا. نظرًا لعدم حساب نتيجة الحقل تلقائيًا ، من المتوقع أن تمرر بعض قيمة السلسلة (أو حتى سلسلة فارغة) التي سيتم إدراجها في نتيجة الحقل. ستبقى هذه القيمة في نتيجة الحقل كعنصر نائب حتى يصبح الحقل updated. لتحديث نتيجة الحقل يمكنك الاتصال[`Update`](../../../aspose.words.fields/field/update)على كائن الحقل الذي تم إرجاعه إليك أو[`UpdateFields`](../../document/updatefields) لتحديث الحقول في المستند بأكمله.

### أمثلة

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

// نقل منشئ المستند إلى العنوان الأساسي للقسم الأول ،
// التي ستعرضها كل صفحة في هذا القسم.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// أدخل حقل PAGE ، والذي سيعرض رقم الصفحة الحالية.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// تكوين القسم بحيث يبدأ عدد الصفحات التي تعرضها حقول PAGE من 5.
// أيضًا ، قم بتكوين جميع حقول PAGE لعرض أرقام الصفحات الخاصة بهم باستخدام الأرقام الرومانية الكبيرة.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// إنشاء رأس أساسي آخر للقسم الثاني ، مع حقل PAGE آخر.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// تكوين القسم بحيث يبدأ عدد الصفحات التي تعرضها حقول PAGE من 10.
// أيضًا ، قم بتكوين جميع حقول PAGE لعرض أرقام الصفحات الخاصة بهم باستخدام الأرقام العربية.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### أنظر أيضا

* class [Field](../../../aspose.words.fields/field)
* class [DocumentBuilder](../../documentbuilder)
* مساحة الاسم [Aspose.Words](../../documentbuilder)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
