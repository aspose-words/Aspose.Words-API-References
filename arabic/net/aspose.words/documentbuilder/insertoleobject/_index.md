---
title: InsertOleObject
second_title: Aspose.Words لمراجع .NET API
description: إدراج كائن OLE مضمن من دفق إلى المستند.
type: docs
weight: 370
url: /ar/net/aspose.words/documentbuilder/insertoleobject/
---
## InsertOleObject(Stream, string, bool, Stream) {#insertoleobject}

إدراج كائن OLE مضمن من دفق إلى المستند.

```csharp
public Shape InsertOleObject(Stream stream, string progId, bool asIcon, Stream presentation)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | دفق يحتوي على بيانات التطبيق. |
| progId | String | معرّف برمجي لكائن OLE. |
| asIcon | Boolean | تحديد الوضع Iconic أو Normal لكائن OLE الجاري إدراجه. |
| presentation | Stream | عرض صورة لكائن OLE. إذا كانت القيمة لاغية ، فستستخدم الكلمات إحدى الصور المحددة مسبقًا. |

### قيمة الإرجاع

عقدة الشكل تحتوي على كائن Ole ويتم إدراجها في موضع Builder الحالي.

### أمثلة

يوضح كيفية استخدام منشئ المستندات لتضمين كائنات OLE في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل جدول بيانات Microsoft Excel من نظام الملفات المحلي
// في المستند مع الاحتفاظ بمظهره الافتراضي.
using (Stream spreadsheetStream = File.Open(MyDir + "Spreadsheet.xlsx", FileMode.Open))
{
    builder.Writeln("Spreadsheet Ole object:");
    // إذا تم حذف "العرض التقديمي" وتعيين "asIcon" ، يتم تحديد طريقة التحميل الزائد هذه
    // الرمز وفقًا لـ "progId" ويستخدم التسمية التوضيحية للأيقونة المحددة مسبقًا.
    builder.InsertOleObject(spreadsheetStream, "OleObject.xlsx", false, null);
}

// إدراج عرض Microsoft Powerpoint ككائن OLE.
// هذه المرة ، سيتم تنزيل صورة من الويب للحصول على رمز.
using (Stream powerpointStream = File.Open(MyDir + "Presentation.pptx", FileMode.Open))
{
    using (WebClient webClient = new WebClient())
    {
        byte[] imgBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

        using (MemoryStream imageStream = new MemoryStream(imgBytes))
        {
            builder.InsertParagraph();
            builder.Writeln("Powerpoint Ole object:");
            builder.InsertOleObject(powerpointStream, "OleObject.pptx", true, imageStream);
        }
    }
}

// انقر نقرًا مزدوجًا فوق هذه الكائنات في Microsoft Word لفتحها
// الملفات المرتبطة باستخدام التطبيقات الخاصة بكل منها.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjects.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertOleObject(string, bool, bool, Stream) {#insertoleobject_1}

إدراج عنصر OLE مضمن أو مرتبط من ملف في المستند. يكتشف نوع كائن OLE باستخدام امتداد الملف.

```csharp
public Shape InsertOleObject(string fileName, bool isLinked, bool asIcon, Stream presentation)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | المسار الكامل للملف. |
| isLinked | Boolean | إذا كانت true ، فسيتم إدراج كائن OLE المرتبط وإلا فسيتم إدراج كائن OLE المضمّن. |
| asIcon | Boolean | تحديد الوضع Iconic أو Normal لكائن OLE الجاري إدراجه. |
| presentation | Stream | عرض صورة لكائن OLE. إذا كانت القيمة لاغية ، فستستخدم الكلمات إحدى الصور المحددة مسبقًا. |

### قيمة الإرجاع

عقدة الشكل تحتوي على كائن Ole ويتم إدراجها في موضع Builder الحالي.

### أمثلة

يوضح كيفية إدراج كائن OLE في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// كائنات OLE هي روابط لملفات في نظام الملفات المحلي لدينا يمكن فتحها بواسطة تطبيقات أخرى مثبتة.
// سيؤدي النقر المزدوج فوق هذه الأشكال إلى تشغيل التطبيق ، ثم استخدامه لفتح الكائن المرتبط.
// هناك ثلاث طرق لاستخدام طريقة InsertOleObject لإدراج هذه الأشكال وتكوين مظهرها.
// 1 - صورة مأخوذة من نظام الملفات المحلي:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // إذا تم حذف "العرض التقديمي" وتعيين "asIcon" ، يتم تحديد طريقة التحميل الزائد هذه
    // الرمز وفقًا لامتداد الملف ويستخدم اسم الملف لتعليق الرمز.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// إذا تم حذف "العرض التقديمي" وتعيين "asIcon" ، يتم تحديد طريقة التحميل الزائد هذه
// الرمز وفقًا لـ "progId" ويستخدم اسم الملف لتعليق الرمز.
// 2 - رمز يعتمد على التطبيق الذي سيفتح الكائن:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// إذا تم حذف 'iconFile' و 'iconCaption' ، فسيتم اختيار طريقة التحميل الزائد هذه
// الرمز وفقًا لـ "progId" ويستخدم التسمية التوضيحية للأيقونة المحددة مسبقًا.
// 3 - رمز الصورة بحجم 32 × 32 بكسل أو أصغر من نظام الملفات المحلي ، مع تسمية توضيحية مخصصة:
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertOleObject(string, string, bool, bool, Stream) {#insertoleobject_2}

إدراج عنصر OLE مضمن أو مرتبط من ملف في المستند. يكتشف نوع كائن OLE باستخدام معلمة progID معينة.

```csharp
public Shape InsertOleObject(string fileName, string progId, bool isLinked, bool asIcon, 
    Stream presentation)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | المسار الكامل للملف. |
| progId | String | ProgId لكائن OLE. |
| isLinked | Boolean | إذا كانت true ، فسيتم إدراج كائن OLE المرتبط وإلا فسيتم إدراج كائن OLE المضمّن. |
| asIcon | Boolean | تحديد الوضع Iconic أو Normal لكائن OLE الجاري إدراجه. |
| presentation | Stream | عرض صورة لكائن OLE. إذا كانت القيمة لاغية ، فستستخدم الكلمات إحدى الصور المحددة مسبقًا. |

### قيمة الإرجاع

عقدة الشكل تحتوي على كائن Ole ويتم إدراجها في موضع Builder الحالي.

### أمثلة

يوضح كيفية إدراج كائن OLE في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// كائنات OLE هي روابط لملفات في نظام الملفات المحلي لدينا يمكن فتحها بواسطة تطبيقات أخرى مثبتة.
// سيؤدي النقر المزدوج فوق هذه الأشكال إلى تشغيل التطبيق ، ثم استخدامه لفتح الكائن المرتبط.
// هناك ثلاث طرق لاستخدام طريقة InsertOleObject لإدراج هذه الأشكال وتكوين مظهرها.
// 1 - صورة مأخوذة من نظام الملفات المحلي:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // إذا تم حذف "العرض التقديمي" وتعيين "asIcon" ، يتم تحديد طريقة التحميل الزائد هذه
    // الرمز وفقًا لامتداد الملف ويستخدم اسم الملف لتعليق الرمز.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// إذا تم حذف "العرض التقديمي" وتعيين "asIcon" ، يتم تحديد طريقة التحميل الزائد هذه
// الرمز وفقًا لـ "progId" ويستخدم اسم الملف لتعليق الرمز.
// 2 - رمز يعتمد على التطبيق الذي سيفتح الكائن:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// إذا تم حذف 'iconFile' و 'iconCaption' ، فسيتم اختيار طريقة التحميل الزائد هذه
// الرمز وفقًا لـ "progId" ويستخدم التسمية التوضيحية للأيقونة المحددة مسبقًا.
// 3 - رمز الصورة بحجم 32 × 32 بكسل أو أصغر من نظام الملفات المحلي ، مع تسمية توضيحية مخصصة:
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
