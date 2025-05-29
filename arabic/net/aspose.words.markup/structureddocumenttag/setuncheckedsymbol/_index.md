---
title: StructuredDocumentTag.SetUncheckedSymbol
linktitle: SetUncheckedSymbol
articleTitle: SetUncheckedSymbol
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل طريقة SetUncheckedSymbol على تعزيز StructuredDocumentTag من خلال تخصيص صور مربع الاختيار لتحسين تجربة المستخدم.
type: docs
weight: 390
url: /ar/net/aspose.words.markup/structureddocumenttag/setuncheckedsymbol/
---
## StructuredDocumentTag.SetUncheckedSymbol method

يحدد الرمز المستخدم لتمثيل حالة عدم تحديد عنصر التحكم في محتوى مربع الاختيار.

```csharp
public void SetUncheckedSymbol(int characterCode, string fontName)
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
