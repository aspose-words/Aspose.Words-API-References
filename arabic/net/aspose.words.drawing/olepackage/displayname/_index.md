---
title: OlePackage.DisplayName
linktitle: DisplayName
articleTitle: DisplayName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية OlePackage DisplayName لإدارة أسماء عرض حزمة OLE بسهولة. حسّن تنظيم بياناتك بهذه الميزة الأساسية.
type: docs
weight: 10
url: /ar/net/aspose.words.drawing/olepackage/displayname/
---
## OlePackage.DisplayName property

يحصل على اسم عرض حزمة OLE أو يعينه.

```csharp
public string DisplayName { get; set; }
```

## أمثلة

يوضح كيفية إدراج كائن OLE في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تسمح لنا كائنات OLE بفتح ملفات أخرى في نظام الملفات المحلي باستخدام تطبيق آخر مثبت
// في نظام التشغيل الخاص بنا عن طريق النقر المزدوج على الشكل الذي يحتوي على كائن OLE في نص المستند.
// في هذه الحالة، سيكون ملفنا الخارجي عبارة عن أرشيف ZIP.
byte[] zipFileBytes = File.ReadAllBytes(DatabaseDir + "cat001.zip");

using (MemoryStream stream = new MemoryStream(zipFileBytes))
{
    Shape shape = builder.InsertOleObject(stream, "Package", true, null);

    shape.OleFormat.OlePackage.FileName = "Package file name.zip";
    shape.OleFormat.OlePackage.DisplayName = "Package display name.zip";
}

doc.Save(ArtifactsDir + "Shape.InsertOlePackage.docx");
```

### أنظر أيضا

* class [OlePackage](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
