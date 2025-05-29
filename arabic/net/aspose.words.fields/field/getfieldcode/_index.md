---
title: Field.GetFieldCode
linktitle: GetFieldCode
articleTitle: GetFieldCode
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة GetFieldCode، واسترجع بسهولة النص بين بداية الحقل والفاصل، بما في ذلك رموز الحقول الفرعية والنتائج. حسّن كفاءة ترميزك!
type: docs
weight: 110
url: /ar/net/aspose.words.fields/field/getfieldcode/
---
## GetFieldCode() {#getfieldcode}

يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية.

```csharp
public string GetFieldCode()
```

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

يوضح كيفية الحصول على رمز حقل الحقل.

```csharp
// افتح مستندًا يحتوي على MERGEFIELD داخل حقل IF.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// هناك طريقتان للحصول على رمز حقل الحقل:
// 1 - حذف الحقول الداخلية:
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - تضمين الحقول الداخلية:
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// بشكل افتراضي، تعرض طريقة GetFieldCode الحقول الداخلية.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### أنظر أيضا

* class [Field](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)

---

## GetFieldCode(*bool*) {#getfieldcode_1}

إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل).

```csharp
public string GetFieldCode(bool includeChildFieldCodes)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| includeChildFieldCodes | Boolean | `حقيقي` إذا كان ينبغي تضمين رموز الحقول الفرعية. |

## أمثلة

يوضح كيفية الحصول على رمز حقل الحقل.

```csharp
// افتح مستندًا يحتوي على MERGEFIELD داخل حقل IF.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// هناك طريقتان للحصول على رمز حقل الحقل:
// 1 - حذف الحقول الداخلية:
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - تضمين الحقول الداخلية:
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// بشكل افتراضي، تعرض طريقة GetFieldCode الحقول الداخلية.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### أنظر أيضا

* class [Field](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
