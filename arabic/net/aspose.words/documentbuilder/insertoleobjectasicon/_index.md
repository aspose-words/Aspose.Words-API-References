---
title: DocumentBuilder.InsertOleObjectAsIcon
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder طريقة. يقوم بإدراج كائن OLE مضمن أو مرتبط كأيقونة في المستند. يسمح بتحديد ملف الرمز والتسمية التوضيحية. يكتشف نوع كائن OLE باستخدام امتداد الملف.
type: docs
weight: 410
url: /ar/net/aspose.words/documentbuilder/insertoleobjectasicon/
---
## InsertOleObjectAsIcon(string, bool, string, string) {#insertoleobjectasicon_1}

يقوم بإدراج كائن OLE مضمن أو مرتبط كأيقونة في المستند. يسمح بتحديد ملف الرمز والتسمية التوضيحية. يكتشف نوع كائن OLE باستخدام امتداد الملف.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, bool isLinked, string iconFile, 
    string iconCaption)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | المسار الكامل للملف . |
| isLinked | Boolean | إذا`حقيقي` ثم يتم إدراج كائن OLE المرتبط وإلا فسيتم إدراج كائن OLE المضمن. |
| iconFile | String | المسار الكامل لملف ICO. إذا كانت القيمة`باطل` ، سوف يستخدم Aspose.Words صورة محددة مسبقًا. |
| iconCaption | String | تسمية توضيحية للرمز. إذا كانت القيمة`باطل` سوف يستخدم Aspose.Words اسم الملف. |

### قيمة الإرجاع

عقدة الشكل تحتوي على كائن Ole وتم إدراجها في موضع Builder الحالي.

### أمثلة

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
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(string, string, bool, string, string) {#insertoleobjectasicon_2}

يقوم بإدراج كائن OLE مضمن أو مرتبط كأيقونة في المستند. يسمح بتحديد ملف الرمز والتسمية التوضيحية. يكتشف نوع كائن OLE باستخدام معلمة progID المحددة.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, string progId, bool isLinked, string iconFile, 
    string iconCaption)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | المسار الكامل للملف . |
| progId | String | ProgId لكائن OLE. |
| isLinked | Boolean | إذا`حقيقي` ثم يتم إدراج كائن OLE المرتبط وإلا فسيتم إدراج كائن OLE المضمن. |
| iconFile | String | المسار الكامل لملف ICO. إذا كانت القيمة`باطل` ، سوف يستخدم Aspose.Words صورة محددة مسبقًا. |
| iconCaption | String | تسمية توضيحية للرمز. إذا كانت القيمة`باطل` سوف يستخدم Aspose.Words اسم الملف. |

### قيمة الإرجاع

عقدة الشكل تحتوي على كائن Ole وتم إدراجها في موضع Builder الحالي.

### أمثلة

يوضح كيفية إدراج كائن OLE مضمن أو مرتبط كأيقونة في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا تم حذف "iconFile" و"iconCaption"، فسيتم تحديد هذه الطريقة المحملة بشكل زائد
// الرمز وفقًا لـ "progId" ويستخدم اسم الملف للتسمية التوضيحية للرمز.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // إذا تم حذف "iconFile" و"iconCaption"، فسيتم تحديد هذه الطريقة المحملة بشكل زائد
    // الرمز وفقًا لامتداد الملف ويستخدم اسم الملف للتسمية التوضيحية للرمز.
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

إدراج كائن OLE مضمن كأيقونة من دفق في المستند. يسمح بتحديد ملف الرمز والتسمية التوضيحية. يكتشف نوع كائن OLE باستخدام معلمة progID المحددة.

```csharp
public Shape InsertOleObjectAsIcon(Stream stream, string progId, string iconFile, 
    string iconCaption)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | تيار يحتوي على بيانات التطبيق. |
| progId | String | ProgId لكائن OLE. |
| iconFile | String | المسار الكامل لملف ICO. إذا كانت القيمة`باطل` ، سوف يستخدم Aspose.Words صورة محددة مسبقًا. |
| iconCaption | String | تسمية توضيحية للرمز. إذا كانت القيمة`باطل` ، سوف يستخدم Aspose.Words تسمية توضيحية محددة مسبقًا للرمز. |

### قيمة الإرجاع

عقدة الشكل تحتوي على كائن Ole وتم إدراجها في موضع Builder الحالي.

### أمثلة

يوضح كيفية إدراج كائن OLE مضمن أو مرتبط كأيقونة في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا تم حذف "iconFile" و"iconCaption"، فسيتم تحديد هذه الطريقة المحملة بشكل زائد
// الرمز وفقًا لـ "progId" ويستخدم اسم الملف للتسمية التوضيحية للرمز.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // إذا تم حذف "iconFile" و"iconCaption"، فسيتم تحديد هذه الطريقة المحملة بشكل زائد
    // الرمز وفقًا لامتداد الملف ويستخدم اسم الملف للتسمية التوضيحية للرمز.
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


