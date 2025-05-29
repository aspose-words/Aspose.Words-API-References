---
title: FieldBuilder
linktitle: FieldBuilder
articleTitle: FieldBuilder
second_title: Aspose.Words لـ .NET
description: اكتشف FieldBuilder، الأداة الفعّالة لإنشاء وإدارة الحقول في مشاريعك بسهولة. بسّط سير عملك اليوم!
type: docs
weight: 10
url: /ar/net/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder constructor

يقوم بتهيئة مثيل لـ[`FieldBuilder`](../) الصف.

```csharp
public FieldBuilder(FieldType fieldType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldType | FieldType | نوع الحقل المراد بنائه. |

## أمثلة

يوضح كيفية إنشاء حقل وإدراجه باستخدام منشئ الحقول.

```csharp
Document doc = new Document();

// الطريقة المريحة لإضافة محتوى نصي إلى مستند هي باستخدام منشئ المستندات.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write(" Hello world! This text is one Run, which is an inline node.");

// تحتوي الحقول على منشئها، والذي يمكننا استخدامه لإنشاء رمز الحقل قطعة قطعة.
// في هذه الحالة، سنقوم بإنشاء حقل BARCODE الذي يمثل الرمز البريدي الأمريكي،
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
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
