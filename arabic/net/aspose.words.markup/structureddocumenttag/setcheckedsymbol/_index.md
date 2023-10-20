---
title: StructuredDocumentTag.SetCheckedSymbol
linktitle: SetCheckedSymbol
articleTitle: SetCheckedSymbol
second_title: Aspose.Words لـ .NET
description: StructuredDocumentTag SetCheckedSymbol طريقة. يعين الرمز المستخدم لتمثيل الحالة المحددة لعنصر تحكم محتوى خانة الاختيار في C#.
type: docs
weight: 360
url: /ar/net/aspose.words.markup/structureddocumenttag/setcheckedsymbol/
---
## StructuredDocumentTag.SetCheckedSymbol method

يعين الرمز المستخدم لتمثيل الحالة المحددة لعنصر تحكم محتوى خانة الاختيار.

```csharp
public void SetCheckedSymbol(int characterCode, string fontName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| characterCode | Int32 | رمز الحرف للرمز المحدد. |
| fontName | String | اسم الخط الذي يحتوي على الرمز. |

## ملاحظات

الوصول إلى هذه الطريقة لن يعمل إلا من أجلCheckbox أنواع المعاملة الخاصة والتفضيلية.

بالنسبة لجميع أنواع SDT الأخرى، سيحدث استثناء.

## أمثلة

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
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
