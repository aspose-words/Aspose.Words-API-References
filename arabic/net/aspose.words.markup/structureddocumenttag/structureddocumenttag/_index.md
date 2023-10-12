---
title: StructuredDocumentTag.StructuredDocumentTag
second_title: Aspose.Words لمراجع .NET API
description: StructuredDocumentTag البناء. تهيئة مثيل جديد لـ علامة الوثيقة المنظمة فئة.
type: docs
weight: 10
url: /ar/net/aspose.words.markup/structureddocumenttag/structureddocumenttag/
---
## StructuredDocumentTag constructor

تهيئة مثيل جديد لـ **علامة الوثيقة المنظمة** فئة.

```csharp
public StructuredDocumentTag(DocumentBase doc, SdtType type, MarkupLevel level)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| doc | DocumentBase | وثيقة المالك. |
| type | SdtType | نوع العقدة SDT. |
| level | MarkupLevel | مستوى عقدة SDT داخل الوثيقة. |

### ملاحظات

يمكن إنشاء الأنواع التالية من المعاملة الخاصة والتفضيلية:

* Checkbox
* DropDownList
* ComboBox
* Date
* BuildingBlockGallery
* Group
* Picture
* RichText
* PlainText

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

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [SdtType](../../sdttype/)
* enum [MarkupLevel](../../markuplevel/)
* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../structureddocumenttag/)
* المجسم [Aspose.Words](../../../)


