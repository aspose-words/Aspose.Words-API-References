---
title: DocumentBuilder.Underline
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية التسطير في DocumentBuilder لتخصيص أنماط الخطوط بسهولة. حسّن مستنداتك بخيارات تسطير متعددة لمظهر احترافي.
type: docs
weight: 190
url: /ar/net/aspose.words/documentbuilder/underline/
---
## DocumentBuilder.Underline property

يحصل على/يحدد نوع التسطير للخط الحالي.

```csharp
public Underline Underline { get; set; }
```

## أمثلة

يوضح كيفية تنسيق النص المدرج بواسطة منشئ المستندات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Dash;
builder.Font.Color = Color.Blue;
builder.Font.Size = 32;

// يقوم المنشئ بتطبيق التنسيق على فقرته الحالية وأي نص جديد تمت إضافته بعد ذلك.
builder.Writeln("Large, blue, and underlined text.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertUnderline.docx");
```

### أنظر أيضا

* enum [Underline](../../underline/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
