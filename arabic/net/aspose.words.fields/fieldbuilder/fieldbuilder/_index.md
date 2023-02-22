---
title: FieldBuilder.FieldBuilder
second_title: Aspose.Words لمراجع .NET API
description: FieldBuilder البناء. يقوم بتهيئة مثيل لملفFieldBuilder فئة .
type: docs
weight: 10
url: /ar/net/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder constructor

يقوم بتهيئة مثيل لملف[`FieldBuilder`](../) فئة .

```csharp
public FieldBuilder(FieldType fieldType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldType | FieldType | نوع الحقل المراد بناؤه. |

### أمثلة

يوضح كيفية إنشاء وإدراج حقل باستخدام منشئ الحقول.

```csharp
Document doc = new Document();

// طريقة مناسبة لإضافة محتوى نصي إلى مستند هي باستخدام أداة إنشاء المستندات.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write(" Hello world! This text is one Run, which is an inline node.");

// الحقول لها منشئها ، والذي يمكننا استخدامه لبناء كود حقل قطعة قطعة.
// في هذه الحالة ، سننشئ حقل BARCODE يمثل رمزًا بريديًا للولايات المتحدة ،
// ثم أدخله أمام Run.
FieldBuilder fieldBuilder = new FieldBuilder(FieldType.FieldBarcode);
fieldBuilder.AddArgument("90210");
fieldBuilder.AddSwitch("\\f", "A");
fieldBuilder.AddSwitch("\\u");

fieldBuilder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph.Runs[0]);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CreateWithFieldBuilder.docx");
```

### أنظر أيضا

* enum [FieldType](../../fieldtype/)
* class [FieldBuilder](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldbuilder/)
* المجسم [Aspose.Words](../../../)


