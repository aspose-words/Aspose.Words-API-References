---
title: StructuredDocumentTag.SetCheckedSymbol
linktitle: SetCheckedSymbol
articleTitle: SetCheckedSymbol
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية استخدام طريقة SetCheckedSymbol في StructuredDocumentTag لتخصيص عناصر مربع الاختيار المرئية وتحسين تجربة المستخدم.
type: docs
weight: 380
url: /ar/net/aspose.words.markup/structureddocumenttag/setcheckedsymbol/
---
## StructuredDocumentTag.SetCheckedSymbol method

يحدد الرمز المستخدم لتمثيل حالة تحديد عنصر التحكم في محتوى مربع الاختيار.

```csharp
public void SetCheckedSymbol(int characterCode, string fontName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| characterCode | Int32 | رمز الحرف للرمز المحدد. |
| fontName | String | اسم الخط الذي يحتوي على الرمز. |

## ملاحظات

الوصول إلى هذه الطريقة سيعمل فقط لـCheckbox أنواع SDT.

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
