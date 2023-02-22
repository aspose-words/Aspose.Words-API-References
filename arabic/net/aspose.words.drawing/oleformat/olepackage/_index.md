---
title: OleFormat.OlePackage
second_title: Aspose.Words لمراجع .NET API
description: OleFormat ملكية. توفير الوصول إلىOlePackage إذا كان كائن OLE عبارة عن حزمة OLE. إرجاع فارغ وإلا .
type: docs
weight: 80
url: /ar/net/aspose.words.drawing/oleformat/olepackage/
---
## OleFormat.OlePackage property

توفير الوصول إلى[`OlePackage`](../../olepackage/) إذا كان كائن OLE عبارة عن حزمة OLE. إرجاع فارغ وإلا .

```csharp
public OlePackage OlePackage { get; }
```

### ملاحظات

حزمة OLE هي تقنية قديمة تسمح بلف أي تنسيق ملف غير موجود في سجل OLE الخاص بنظام Windows في حزمة عامة تسمح بتضمين أي شيء تقريبًا في مستند. انظر[`OlePackage`](../../olepackage/)اكتب لمزيد من المعلومات.

### أمثلة

يوضح كيفية إدراج كائن OLE في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تسمح لنا كائنات OLE بفتح ملفات أخرى في نظام الملفات المحلي باستخدام تطبيق آخر مثبت
// في نظام التشغيل لدينا عن طريق النقر المزدوج على الشكل الذي يحتوي على كائن OLE في نص المستند.
// في هذه الحالة ، سيكون ملفنا الخارجي عبارة عن أرشيف بتنسيق ZIP.
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
* مساحة الاسم [Aspose.Words.Drawing](../../oleformat/)
* المجسم [Aspose.Words](../../../)


