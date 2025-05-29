---
title: FieldTC Class
linktitle: FieldTC
articleTitle: FieldTC
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FieldTC لتنفيذ حقل TC بسلاسة، مما يعزز معالجة المستندات لديك بميزات قوية.
type: docs
weight: 2890
url: /ar/net/aspose.words.fields/fieldtc/
---
## FieldTC class

ينفذ حقل TC.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public sealed class FieldTC : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldTC](fieldtc/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [EntryLevel](../../aspose.words.fields/fieldtc/entrylevel/) { get; set; } | يحصل على مستوى الإدخال أو يعينه. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/)الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | يحصل على أو يحدد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | يحصل على أو يحدد ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب نتيجته). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | يحصل على أو يعين LCID للحقل. |
| [OmitPageNumber](../../aspose.words.fields/fieldtc/omitpagenumber/) { get; set; } | يحصل على أو يحدد ما إذا كان يجب حذف رقم الصفحة في جدول المحتويات لهذا الحقل. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | يحصل على النص الموجود بين فاصل الحقل ونهاية الحقل أو يعينه. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن يكون`باطل` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [Text](../../aspose.words.fields/fieldtc/text/) { get; set; } | يحصل على نص الإدخال أو يعينه. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | يحصل على نوع حقل Microsoft Word. |
| [TypeIdentifier](../../aspose.words.fields/fieldtc/typeidentifier/) { get; set; } | يحصل على معرف نوع لهذا الحقل (وهو عادةً حرف) أو يعينه. |

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

يحدد النص ورقم الصفحة لإدخال جدول المحتويات (بما في ذلك جدول الأشكال)، والذي يستخدمه حقل جدول المحتويات.

## أمثلة

يوضح كيفية إدراج حقل جدول المحتويات، وتصفية حقول جدول المحتويات التي تنتهي كإدخالات.

```csharp
public void FieldTocEntryIdentifier()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // قم بإدراج حقل جدول المحتويات، والذي سيقوم بتجميع كل حقول جدول المحتويات في جدول المحتويات.
    FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // قم بتكوين الحقل فقط لالتقاط إدخالات TC من النوع "A"، ومستوى الإدخال بين 1 و3.
    fieldToc.EntryIdentifier = "A";
    fieldToc.EntryLevelRange = "1-3";

    Assert.AreEqual(" TOC  \\f A \\l 1-3", fieldToc.GetFieldCode());

    //سيظهر هذان الإدخالان في الجدول.
    builder.InsertBreak(BreakType.PageBreak);
    InsertTocEntry(builder, "TC field 1", "A", "1");
    InsertTocEntry(builder, "TC field 2", "A", "2");

    Assert.AreEqual(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.Range.Fields[1].GetFieldCode());

    //سيتم حذف هذا الإدخال من الجدول لأنه من نوع مختلف عن "A".
    InsertTocEntry(builder, "TC field 3", "B", "1");

    // سيتم حذف هذا الإدخال من الجدول لأنه يحتوي على مستوى إدخال خارج النطاق 1-3.
    InsertTocEntry(builder, "TC field 4", "A", "5");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TC.docx");
}

/// <summary>
/// استخدم منشئ المستندات لإدراج حقل TC.
/// </summary>
public void InsertTocEntry(DocumentBuilder builder, string text, string typeIdentifier, string entryLevel)
{
    FieldTC fieldTc = (FieldTC)builder.InsertField(FieldType.FieldTOCEntry, true);
    fieldTc.OmitPageNumber = true;
    fieldTc.Text = text;
    fieldTc.TypeIdentifier = typeIdentifier;
    fieldTc.EntryLevel = entryLevel;
}
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
