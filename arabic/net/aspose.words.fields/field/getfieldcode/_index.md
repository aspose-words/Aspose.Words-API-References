---
title: Field.GetFieldCode
second_title: Aspose.Words لمراجع .NET API
description: Field طريقة. إرجاع النص بين بداية الحقل وفاصل الحقل أو نهاية الحقل إذا لم يكن هناك فاصل. يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية.
type: docs
weight: 110
url: /ar/net/aspose.words.fields/field/getfieldcode/
---
## GetFieldCode() {#getfieldcode}

إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية.

```csharp
public string GetFieldCode()
```

### أمثلة

يوضح كيفية إدراج حقل في مستند باستخدام رمز الحقل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// هذا التحميل الزائد لطريقة InsertField يقوم تلقائيًا بتحديث الحقول المدرجة.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

يوضح كيفية الحصول على رمز الحقل الخاص بالحقل.

```csharp
// افتح مستندًا يحتوي على MERGEFIELD داخل حقل IF.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// هناك طريقتان للحصول على رمز الحقل:
// 1 - حذف حقوله الداخلية:
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - تضمين حقوله الداخلية:
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// افتراضيًا، تعرض طريقة GetFieldCode الحقول الداخلية.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### أنظر أيضا

* class [Field](../)
* مساحة الاسم [Aspose.Words.Fields](../../field/)
* المجسم [Aspose.Words](../../../)

---

## GetFieldCode(bool) {#getfieldcode_1}

إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل).

```csharp
public string GetFieldCode(bool includeChildFieldCodes)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| includeChildFieldCodes | Boolean | `حقيقي` إذا كان يجب تضمين رموز الحقول الفرعية. |

### أمثلة

يوضح كيفية الحصول على رمز الحقل الخاص بالحقل.

```csharp
// افتح مستندًا يحتوي على MERGEFIELD داخل حقل IF.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// هناك طريقتان للحصول على رمز الحقل:
// 1 - حذف حقوله الداخلية:
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - تضمين حقوله الداخلية:
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// افتراضيًا، تعرض طريقة GetFieldCode الحقول الداخلية.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### أنظر أيضا

* class [Field](../)
* مساحة الاسم [Aspose.Words.Fields](../../field/)
* المجسم [Aspose.Words](../../../)


