---
title: DocumentBuilder.InsertOleObjectAsIcon
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder طريقة. إدراج كائن OLE مضمن أو مرتبط كرمز في المستند. يسمح بتحديد ملف الرمز والتسمية التوضيحية. يكتشف نوع كائن OLE باستخدام امتداد الملف.
type: docs
weight: 380
url: /ar/net/aspose.words/documentbuilder/insertoleobjectasicon/
---
## InsertOleObjectAsIcon(string, bool, string, string) {#insertoleobjectasicon_1}

إدراج كائن OLE مضمن أو مرتبط كرمز في المستند. يسمح بتحديد ملف الرمز والتسمية التوضيحية. يكتشف نوع كائن OLE باستخدام امتداد الملف.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, bool isLinked, string iconFile, 
    string iconCaption)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | المسار الكامل للملف. |
| isLinked | Boolean | إذا كانت القيمة صحيحة ، فسيتم إدراج كائن OLE المرتبط وإلا فسيتم إدراج كائن OLE المضمّن. |
| iconFile | String | المسار الكامل لملف ICO. إذا كانت القيمة خالية ، فستستخدم Aspose.Words صورة محددة مسبقًا. |
| iconCaption | String | التسمية التوضيحية للرمز. إذا كانت القيمة خالية ، فسيستخدم Aspose.Words اسم الملف. |

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

## InsertOleObjectAsIcon(string, string, bool, string, string) {#insertoleobjectasicon_2}

إدراج كائن OLE مضمن أو مرتبط كرمز في المستند. يسمح بتحديد ملف الرمز والتسمية التوضيحية. يكتشف نوع كائن OLE باستخدام معلمة progID معينة.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, string progId, bool isLinked, string iconFile, 
    string iconCaption)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | المسار الكامل للملف. |
| progId | String | ProgId لكائن OLE. |
| isLinked | Boolean | إذا كانت القيمة صحيحة ، فسيتم إدراج كائن OLE المرتبط وإلا فسيتم إدراج كائن OLE المضمّن. |
| iconFile | String | المسار الكامل لملف ICO. إذا كانت القيمة خالية ، فستستخدم Aspose.Words صورة محددة مسبقًا. |
| iconCaption | String | التسمية التوضيحية للرمز. إذا كانت القيمة خالية ، فسيستخدم Aspose.Words اسم الملف. |

### قيمة الإرجاع

عقدة الشكل تحتوي على كائن Ole ويتم إدراجها في موضع Builder الحالي.

### أمثلة

يوضح كيفية إدراج كائن OLE مضمن أو مرتبط كرمز في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا تم حذف 'iconFile' و 'iconCaption' ، فسيتم اختيار طريقة التحميل الزائد هذه
// الرمز وفقًا لـ "progId" ويستخدم اسم الملف لتعليق الرمز.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // إذا تم حذف 'iconFile' و 'iconCaption' ، فسيتم اختيار طريقة التحميل الزائد هذه
    // الرمز وفقًا لامتداد الملف ويستخدم اسم الملف لتعليق الرمز.
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(Stream, string, string, string) {#insertoleobjectasicon}

إدراج كائن OLE مضمن كرمز من تدفق إلى المستند. يسمح بتحديد ملف الرمز والتسمية التوضيحية. يكتشف نوع كائن OLE باستخدام معلمة progID معينة.

```csharp
public Shape InsertOleObjectAsIcon(Stream stream, string progId, string iconFile, 
    string iconCaption)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | دفق يحتوي على بيانات التطبيق. |
| progId | String | ProgId لكائن OLE. |
| iconFile | String | المسار الكامل لملف ICO. إذا كانت القيمة خالية ، فستستخدم Aspose.Words صورة محددة مسبقًا. |
| iconCaption | String | التسمية التوضيحية للرمز. إذا كانت القيمة خالية ، فسيستخدم Aspose.Words تسمية توضيحية للأيقونة محددة مسبقًا. |

### قيمة الإرجاع

عقدة الشكل تحتوي على كائن Ole ويتم إدراجها في موضع Builder الحالي.

### أمثلة

يوضح كيفية إدراج كائن OLE مضمن أو مرتبط كرمز في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا تم حذف 'iconFile' و 'iconCaption' ، فسيتم اختيار طريقة التحميل الزائد هذه
// الرمز وفقًا لـ "progId" ويستخدم اسم الملف لتعليق الرمز.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // إذا تم حذف 'iconFile' و 'iconCaption' ، فسيتم اختيار طريقة التحميل الزائد هذه
    // الرمز وفقًا لامتداد الملف ويستخدم اسم الملف لتعليق الرمز.
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### أنظر أيضا

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)


