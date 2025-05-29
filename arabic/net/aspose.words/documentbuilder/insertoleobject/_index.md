---
title: DocumentBuilder.InsertOleObject
linktitle: InsertOleObject
articleTitle: InsertOleObject
second_title: Aspose.Words لـ .NET
description: قم بتعزيز مستنداتك بسهولة باستخدام طريقة InsertOleObject في DocumentBuilder، مما يسمح بتضمين كائنات OLE من التدفقات بسلاسة.
type: docs
weight: 420
url: /ar/net/aspose.words/documentbuilder/insertoleobject/
---
## InsertOleObject(*Stream, string, bool, Stream*) {#insertoleobject}

يقوم بإدراج كائن OLE مضمن من مجرى إلى المستند.

```csharp
public Shape InsertOleObject(Stream stream, string progId, bool asIcon, Stream presentation)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | تيار يحتوي على بيانات التطبيق. |
| progId | String | معرف برمجي لكائن OLE. |
| asIcon | Boolean | يحدد الوضع الأيقوني أو العادي لكائن OLE الذي يتم إدراجه. |
| presentation | Stream | عرض صورة لكائن OLE. إذا كانت القيمة`باطل` سيستخدم Aspose.Words إحدى الصور المحددة مسبقًا. |

### قيمة الإرجاع

عقدة الشكل التي تحتوي على كائن Ole والمدرجة في موضع المنشئ الحالي.

## أمثلة

يوضح كيفية استخدام منشئ المستندات لتضمين كائنات OLE في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إدراج جدول بيانات Microsoft Excel من نظام الملفات المحلي
// في المستند مع الحفاظ على مظهره الافتراضي.
using (Stream spreadsheetStream = File.Open(MyDir + "Spreadsheet.xlsx", FileMode.Open))
{
    builder.Writeln("Spreadsheet Ole object:");
    // إذا تم حذف "presentation" وتم تعيين "asIcon"، فإن هذه الطريقة المحملة تحدد
    // الرمز وفقًا لـ 'progId' ويستخدم تسمية الرمز المحددة مسبقًا.
    builder.InsertOleObject(spreadsheetStream, "OleObject.xlsx", false, null);
}

// إدراج عرض تقديمي لـ Microsoft Powerpoint ككائن OLE.
// هذه المرة، سيكون هناك صورة تم تنزيلها من الويب لأيقونة.
using (Stream powerpointStream = File.Open(MyDir + "Presentation.pptx", FileMode.Open))
{
    byte[] imgBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

    using (MemoryStream imageStream = new MemoryStream(imgBytes))
    {
        builder.InsertParagraph();
        builder.Writeln("Powerpoint Ole object:");
        builder.InsertOleObject(powerpointStream, "OleObject.pptx", true, imageStream);
    }
}

// انقر نقرًا مزدوجًا فوق هذه الكائنات في Microsoft Word لفتحها
//الملفات المرتبطة باستخدام التطبيقات الخاصة بها.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjects.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertOleObject(*string, bool, bool, Stream*) {#insertoleobject_1}

يُدرج كائن OLE مُضمّنًا أو مُرتبطًا من ملف إلى المستند. يكتشف نوع كائن OLE باستخدام امتداد الملف.

```csharp
public Shape InsertOleObject(string fileName, bool isLinked, bool asIcon, Stream presentation)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | المسار الكامل للملف. |
| isLinked | Boolean | لو`حقيقي`ثم يتم إدراج كائن OLE المرتبط، وإلا يتم إدراج كائن OLE المضمن. |
| asIcon | Boolean | يحدد الوضع الأيقوني أو العادي لكائن OLE الذي يتم إدراجه. |
| presentation | Stream | عرض صورة لكائن OLE. إذا كانت القيمة`باطل` سيستخدم Aspose.Words إحدى الصور المحددة مسبقًا. |

### قيمة الإرجاع

عقدة الشكل التي تحتوي على كائن Ole والمدرجة في موضع المنشئ الحالي.

## أمثلة

يوضح كيفية إدراج كائن OLE في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تعتبر كائنات OLE عبارة عن روابط للملفات الموجودة في نظام الملفات المحلي لدينا والتي يمكن فتحها بواسطة التطبيقات المثبتة الأخرى.
// النقر المزدوج على هذه الأشكال سيؤدي إلى تشغيل التطبيق، ثم استخدامه لفتح الكائن المرتبط.
// هناك ثلاث طرق لاستخدام طريقة InsertOleObject لإدراج هذه الأشكال وتكوين مظهرها.
// 1 - الصورة مأخوذة من نظام الملفات المحلي:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // إذا تم حذف "presentation" وتم تعيين "asIcon"، فإن هذه الطريقة المحملة تحدد
    // الرمز وفقًا لامتداد الملف ويستخدم اسم الملف لعنوان الرمز.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// إذا تم حذف "presentation" وتم تعيين "asIcon"، فإن هذه الطريقة المحملة تحدد
// الرمز وفقًا لـ 'progId' ويستخدم اسم الملف لعنوان الرمز.
// 2 - أيقونة بناءً على التطبيق الذي سيفتح الكائن:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// إذا تم حذف 'iconFile' و'iconCaption'، فإن هذه الطريقة المحملة تختار
// الرمز وفقًا لـ 'progId' ويستخدم تسمية الرمز المحددة مسبقًا.
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

يُدرج كائن OLE مُضمّنًا أو مُرتبطًا من ملف إلى المستند. يكتشف نوع كائن OLE باستخدام مُعامل progID المُعطى.

```csharp
public Shape InsertOleObject(string fileName, string progId, bool isLinked, bool asIcon, 
    Stream presentation)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | المسار الكامل للملف. |
| progId | String | معرف برنامج كائن OLE. |
| isLinked | Boolean | لو`حقيقي`ثم يتم إدراج كائن OLE المرتبط، وإلا يتم إدراج كائن OLE المضمن. |
| asIcon | Boolean | يحدد الوضع الأيقوني أو العادي لكائن OLE الذي يتم إدراجه. |
| presentation | Stream | عرض صورة لكائن OLE. إذا كانت القيمة`باطل` سيستخدم Aspose.Words إحدى الصور المحددة مسبقًا. |

### قيمة الإرجاع

عقدة الشكل التي تحتوي على كائن Ole والمدرجة في موضع المنشئ الحالي.

## أمثلة

يوضح كيفية إدراج كائن OLE في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تعتبر كائنات OLE عبارة عن روابط للملفات الموجودة في نظام الملفات المحلي لدينا والتي يمكن فتحها بواسطة التطبيقات المثبتة الأخرى.
// النقر المزدوج على هذه الأشكال سيؤدي إلى تشغيل التطبيق، ثم استخدامه لفتح الكائن المرتبط.
// هناك ثلاث طرق لاستخدام طريقة InsertOleObject لإدراج هذه الأشكال وتكوين مظهرها.
// 1 - الصورة مأخوذة من نظام الملفات المحلي:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // إذا تم حذف "presentation" وتم تعيين "asIcon"، فإن هذه الطريقة المحملة تحدد
    // الرمز وفقًا لامتداد الملف ويستخدم اسم الملف لعنوان الرمز.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// إذا تم حذف "presentation" وتم تعيين "asIcon"، فإن هذه الطريقة المحملة تحدد
// الرمز وفقًا لـ 'progId' ويستخدم اسم الملف لعنوان الرمز.
// 2 - أيقونة بناءً على التطبيق الذي سيفتح الكائن:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// إذا تم حذف 'iconFile' و'iconCaption'، فإن هذه الطريقة المحملة تختار
// الرمز وفقًا لـ 'progId' ويستخدم تسمية الرمز المحددة مسبقًا.
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
