---
title: StructuredDocumentTag
linktitle: StructuredDocumentTag
articleTitle: StructuredDocumentTag
second_title: Aspose.Words لـ .NET
description: أنشئ مستندات قوية ومنظمة بسهولة باستخدام مُنشئ StructuredDocumentTag. جهّز نماذج جديدة لتحسين التنظيم والوضوح.
type: docs
weight: 10
url: /ar/net/aspose.words.markup/structureddocumenttag/structureddocumenttag/
---
## StructuredDocumentTag constructor

يقوم بتهيئة مثيل جديد لـ**علامة المستند المنظم** الصف.

```csharp
public StructuredDocumentTag(DocumentBase doc, SdtType type, MarkupLevel level)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| doc | DocumentBase | وثيقة المالك. |
| type | SdtType | نوع عقدة SDT. |
| level | MarkupLevel | مستوى عقدة SDT ضمن المستند. |

## ملاحظات

يمكن إنشاء الأنواع التالية من SDT:

* Checkbox
* DropDownList
* ComboBox
* Date
* BuildingBlockGallery
* Group
* Picture
* RichText
* PlainText

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

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [SdtType](../../sdttype/)
* enum [MarkupLevel](../../markuplevel/)
* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
