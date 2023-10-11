---
title: StructuredDocumentTag.Checked
second_title: Aspose.Words لمراجع .NET API
description: StructuredDocumentTag ملكية. الحصول على/تعيين الحالة الحالية لمربع الاختيار المعاملة الخاصة والتفضيلية . القيمة الافتراضية لهذه الخاصية هيخطأ شنيع .
type: docs
weight: 60
url: /ar/net/aspose.words.markup/structureddocumenttag/checked/
---
## StructuredDocumentTag.Checked property

الحصول على/تعيين الحالة الحالية لمربع الاختيار **المعاملة الخاصة والتفضيلية** . القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` .

```csharp
public bool Checked { get; set; }
```

### ملاحظات

الوصول إلى هذه الخاصية سوف يعمل فقط من أجلCheckbox أنواع المعاملة الخاصة والتفضيلية.

بالنسبة لجميع أنواع SDT الأخرى، سيحدث استثناء.

### أمثلة

أظهر كيفية إنشاء علامة مستند منظمة على شكل مربع اختيار.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

StructuredDocumentTag sdtCheckBox =
    new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline) {Checked = true};

// يمكننا تعيين الرموز المستخدمة لتمثيل الحالة المحددة/غير المحددة لعنصر التحكم في محتوى مربع الاختيار.
sdtCheckBox.SetCheckedSymbol(0x00A9, "Times New Roman");
sdtCheckBox.SetUncheckedSymbol(0x00AE, "Times New Roman");

builder.InsertNode(sdtCheckBox);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CheckBox.docx");
```

### أنظر أيضا

* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../structureddocumenttag/)
* المجسم [Aspose.Words](../../../)


