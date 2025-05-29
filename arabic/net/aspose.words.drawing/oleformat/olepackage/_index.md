---
title: OleFormat.OlePackage
linktitle: OlePackage
articleTitle: OlePackage
second_title: Aspose.Words لـ .NET
description: الوصول إلى خصائص OlePackage لكائنات OLE بسهولة. تمتع بتكامل سلس مع حزم OLE، وحسّن قدراتك على معالجة البيانات.
type: docs
weight: 80
url: /ar/net/aspose.words.drawing/oleformat/olepackage/
---
## OleFormat.OlePackage property

توفير الوصول إلى[`OlePackage`](../../olepackage/) إذا كان كائن OLE عبارة عن حزمة OLE. يتم إرجاعها`باطل` وإلا.

```csharp
public OlePackage OlePackage { get; }
```

## ملاحظات

حزمة OLE هي تقنية قديمة تسمح بتغليف أي تنسيق ملف غير موجود في سجل OLE الخاص بـ نظام Windows في حزمة عامة تسمح بتضمين أي شيء تقريبًا في مستند. انظر[`OlePackage`](../../olepackage/) اكتب للحصول على مزيد من المعلومات.

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

* class [OlePackage](../../olepackage/)
* class [OleFormat](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
