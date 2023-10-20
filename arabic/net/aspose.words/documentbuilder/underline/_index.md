---
title: DocumentBuilder.Underline
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words لـ .NET
description: DocumentBuilder Underline ملكية. يحصل على/يحدد نوع التسطير للخط الحالي في C#.
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

// يطبق المنشئ التنسيق على فقرته الحالية وأي نص جديد يضاف بواسطته بعد ذلك.
builder.Writeln("Large, blue, and underlined text.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertUnderline.docx");
```

### أنظر أيضا

* enum [Underline](../../underline/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
