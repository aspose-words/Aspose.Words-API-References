---
title: StructuredDocumentTag.Checked
linktitle: Checked
articleTitle: Checked
second_title: Aspose.Words لـ .NET
description: إدارة خانة الاختيار SDT باستخدام خاصية StructuredDocumentTag Checked. احصل على حالتها/عيّنها بسهولة - القيمة الافتراضية هي False. حسّن تفاعلية المستندات اليوم!
type: docs
weight: 60
url: /ar/net/aspose.words.markup/structureddocumenttag/checked/
---
## StructuredDocumentTag.Checked property

يحصل على/يحدد الحالة الحالية لمربع الاختيار**SDT** . القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` .

```csharp
public bool Checked { get; set; }
```

## ملاحظات

سيتم الوصول إلى هذه الخاصية فقط لـCheckbox أنواع SDT.

بالنسبة لجميع أنواع SDT الأخرى، سيحدث استثناء.

## أمثلة

إظهار كيفية إنشاء علامة مستند منظمة في شكل مربع اختيار.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

StructuredDocumentTag sdtCheckBox =
    new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline) { Checked = true };

// يمكننا تعيين الرموز المستخدمة لتمثيل حالة التحديد/عدم التحديد لمحتوى مربع الاختيار.
sdtCheckBox.SetCheckedSymbol(0x00A9, "Times New Roman");
sdtCheckBox.SetUncheckedSymbol(0x00AE, "Times New Roman");

builder.InsertNode(sdtCheckBox);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CheckBox.docx");
```

### أنظر أيضا

* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
