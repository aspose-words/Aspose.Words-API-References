---
title: DocumentBuilder.InsertOleObject
linktitle: InsertOleObject
articleTitle: InsertOleObject
second_title: Aspose.Words لـ .NET
description: DocumentBuilder InsertOleObject طريقة. إدراج كائن OLE مضمن من دفق في المستند في C#.
type: docs
weight: 390
url: /ar/net/aspose.words/documentbuilder/insertoleobject/
---
## InsertOleObject(*Stream, string, bool, Stream*) {#insertoleobject}

إدراج كائن OLE مضمن من دفق في المستند.

```csharp
public Shape InsertOleObject(Stream stream, string progId, bool asIcon, Stream presentation)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | تيار يحتوي على بيانات التطبيق. |
| progId | String | المعرف البرمجي لكائن OLE. |
| asIcon | Boolean | يحدد إما الوضع Iconic أو Normal لكائن OLE الذي يتم إدراجه. |
| presentation | Stream | عرض صورة لكائن OLE. إذا كانت القيمة`باطل` سيستخدم Aspose.Words إحدى الصور المحددة مسبقًا. |

### قيمة الإرجاع

عقدة الشكل تحتوي على كائن Ole وتم إدراجها في موضع Builder الحالي.

## أمثلة

يوضح كيفية استخدام منشئ المستندات لتضمين كائنات OLE في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل جدول بيانات Microsoft Excel من نظام الملفات المحلي
// في المستند مع الاحتفاظ بمظهره الافتراضي.
using (Stream spreadsheetStream = File.Open(MyDir + "Spreadsheet.xlsx", FileMode.Open))
{
    builder.Writeln("Spreadsheet Ole object:");
    // إذا تم حذف "العرض التقديمي" وتعيين "asIcon"، فسيتم تحديد هذه الطريقة المحملة بشكل زائد
    // الأيقونة وفقًا لـ "progId" وتستخدم تسمية توضيحية محددة مسبقًا للرمز.
    builder.InsertOleObject(spreadsheetStream, "OleObject.xlsx", false, null);
}

// قم بإدراج عرض تقديمي لـ Microsoft Powerpoint ككائن OLE.
// هذه المرة، سيكون به صورة تم تنزيلها من الويب للحصول على رمز.
using (Stream powerpointStream = File.Open(MyDir + "Presentation.pptx", FileMode.Open))
{
    using (HttpClient httpClient = new HttpClient())
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
// الملفات المرتبطة باستخدام التطبيقات الخاصة بها.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjects.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertOleObject(*string, bool, bool, Stream*) {#insertoleobject_1}

يقوم بإدراج كائن OLE مضمن أو مرتبط من ملف في المستند. يكتشف نوع كائن OLE باستخدام امتداد الملف.

```csharp
public Shape InsertOleObject(string fileName, bool isLinked, bool asIcon, Stream presentation)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | المسار الكامل للملف . |
| isLinked | Boolean | لو`حقيقي` ثم يتم إدراج كائن OLE المرتبط وإلا يتم إدراج كائن OLE المضمن. |
| asIcon | Boolean | يحدد إما الوضع Iconic أو Normal لكائن OLE الذي يتم إدراجه. |
| presentation | Stream | عرض صورة لكائن OLE. إذا كانت القيمة`باطل` سيستخدم Aspose.Words إحدى الصور المحددة مسبقًا. |

### قيمة الإرجاع

عقدة الشكل تحتوي على كائن Ole وتم إدراجها في موضع Builder الحالي.

## أمثلة

يوضح كيفية إدراج كائن OLE في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// كائنات OLE هي روابط للملفات الموجودة في نظام الملفات المحلي لدينا والتي يمكن فتحها بواسطة التطبيقات المثبتة الأخرى.
// سيؤدي النقر المزدوج على هذه الأشكال إلى تشغيل التطبيق، ثم استخدامه لفتح الكائن المرتبط.
// هناك ثلاث طرق لاستخدام طريقة InsertOleObject لإدراج هذه الأشكال وتكوين مظهرها.
// 1 - الصورة مأخوذة من نظام الملفات المحلي:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // إذا تم حذف "العرض التقديمي" وتعيين "asIcon"، فسيتم تحديد هذه الطريقة المحملة بشكل زائد
    // الرمز وفقًا لامتداد الملف ويستخدم اسم الملف للتسمية التوضيحية للرمز.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// إذا تم حذف "العرض التقديمي" وتعيين "asIcon"، فسيتم تحديد هذه الطريقة المحملة بشكل زائد
// الرمز وفقًا لـ "progId" ويستخدم اسم الملف للتسمية التوضيحية للرمز.
// 2 - أيقونة تعتمد على التطبيق الذي سيفتح الكائن:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// إذا تم حذف "iconFile" و"iconCaption"، فسيتم تحديد هذه الطريقة المحملة بشكل زائد
// الأيقونة وفقًا لـ "progId" وتستخدم تسمية توضيحية محددة مسبقًا للرمز.
// 3 - أيقونة صورة بحجم 32 × 32 بكسل أو أصغر من نظام الملفات المحلي، مع تسمية توضيحية مخصصة:
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertOleObject(*string, string, bool, bool, Stream*) {#insertoleobject_2}

يقوم بإدراج كائن OLE مضمن أو مرتبط من ملف في المستند. يكتشف نوع كائن OLE باستخدام معلمة progID المحددة.

```csharp
public Shape InsertOleObject(string fileName, string progId, bool isLinked, bool asIcon, 
    Stream presentation)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | المسار الكامل للملف . |
| progId | String | ProgId لكائن OLE. |
| isLinked | Boolean | لو`حقيقي` ثم يتم إدراج كائن OLE المرتبط وإلا يتم إدراج كائن OLE المضمن. |
| asIcon | Boolean | يحدد إما الوضع Iconic أو Normal لكائن OLE الذي يتم إدراجه. |
| presentation | Stream | عرض صورة لكائن OLE. إذا كانت القيمة`باطل` سيستخدم Aspose.Words إحدى الصور المحددة مسبقًا. |

### قيمة الإرجاع

عقدة الشكل تحتوي على كائن Ole وتم إدراجها في موضع Builder الحالي.

## أمثلة

يوضح كيفية إدراج كائن OLE في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// كائنات OLE هي روابط للملفات الموجودة في نظام الملفات المحلي لدينا والتي يمكن فتحها بواسطة التطبيقات المثبتة الأخرى.
// سيؤدي النقر المزدوج على هذه الأشكال إلى تشغيل التطبيق، ثم استخدامه لفتح الكائن المرتبط.
// هناك ثلاث طرق لاستخدام طريقة InsertOleObject لإدراج هذه الأشكال وتكوين مظهرها.
// 1 - الصورة مأخوذة من نظام الملفات المحلي:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // إذا تم حذف "العرض التقديمي" وتعيين "asIcon"، فسيتم تحديد هذه الطريقة المحملة بشكل زائد
    // الرمز وفقًا لامتداد الملف ويستخدم اسم الملف للتسمية التوضيحية للرمز.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// إذا تم حذف "العرض التقديمي" وتعيين "asIcon"، فسيتم تحديد هذه الطريقة المحملة بشكل زائد
// الرمز وفقًا لـ "progId" ويستخدم اسم الملف للتسمية التوضيحية للرمز.
// 2 - أيقونة تعتمد على التطبيق الذي سيفتح الكائن:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// إذا تم حذف "iconFile" و"iconCaption"، فسيتم تحديد هذه الطريقة المحملة بشكل زائد
// الأيقونة وفقًا لـ "progId" وتستخدم تسمية توضيحية محددة مسبقًا للرمز.
// 3 - أيقونة صورة بحجم 32 × 32 بكسل أو أصغر من نظام الملفات المحلي، مع تسمية توضيحية مخصصة:
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
