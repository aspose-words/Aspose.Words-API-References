---
title: OleFormat.OlePackage
second_title: Aspose.Words لمراجع .NET API
description: OleFormat ملكية. توفير الوصول إلىOlePackage إذا كان كائن OLE عبارة عن حزمة OLE. Returnsباطل وإلا.
type: docs
weight: 80
url: /ar/net/aspose.words.drawing/oleformat/olepackage/
---
## OleFormat.OlePackage property

توفير الوصول إلى[`OlePackage`](../../olepackage/) إذا كان كائن OLE عبارة عن حزمة OLE. Returns`باطل` وإلا.

```csharp
public OlePackage OlePackage { get; }
```

### ملاحظات

حزمة OLE هي تقنية قديمة تسمح بتغليف أي تنسيق ملف غير موجود في سجل OLE الخاص بـ نظام Windows في حزمة عامة تسمح بتضمين أي شيء تقريبًا في المستند. راجع[`OlePackage`](../../olepackage/) اكتب لمزيد من المعلومات.

### أمثلة

يوضح كيفية إدراج كائن OLE في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تسمح لنا كائنات OLE بفتح ملفات أخرى في نظام الملفات المحلي باستخدام تطبيق آخر مثبت
// في نظام التشغيل الخاص بنا عن طريق النقر المزدوج على الشكل الذي يحتوي على كائن OLE في نص المستند.
// في هذه الحالة، سيكون ملفنا الخارجي عبارة عن أرشيف مضغوط بتنسيق ZIP.
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


