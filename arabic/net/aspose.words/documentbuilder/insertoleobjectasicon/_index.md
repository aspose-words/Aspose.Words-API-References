---
title: DocumentBuilder.InsertOleObjectAsIcon
linktitle: InsertOleObjectAsIcon
articleTitle: InsertOleObjectAsIcon
second_title: Aspose.Words لـ .NET
description: أدرج كائنات OLE كأيقونات في مستنداتك بسهولة باستخدام DocumentBuilder. خصّص الأيقونات والتعليقات التوضيحية مع ضمان التكامل السلس.
type: docs
weight: 430
url: /ar/net/aspose.words/documentbuilder/insertoleobjectasicon/
---
## InsertOleObjectAsIcon(*string, bool, string, string*) {#insertoleobjectasicon_1}

يُدرج كائن OLE مُضمّنًا أو مُرتبطًا كأيقونة في المستند. يسمح بتحديد ملف الأيقونة والتسمية التوضيحية. يكتشف نوع كائن OLE باستخدام امتداد الملف.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, bool isLinked, string iconFile, 
    string iconCaption)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | المسار الكامل للملف. |
| isLinked | Boolean | إذا`حقيقي` ثم يتم إدراج كائن OLE المرتبط، وإلا يتم إدراج كائن OLE المضمن. |
| iconFile | String | المسار الكامل لملف ICO. إذا كانت القيمة`باطل` ، سوف يستخدم Aspose.Words صورة محددة مسبقًا. |
| iconCaption | String | عنوان الرمز. إذا كانت القيمة`باطل` سوف يستخدم Aspose.Words اسم الملف. |

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

## InsertOleObjectAsIcon(*string, string, bool, string, string*) {#insertoleobjectasicon_2}

يُدرج كائن OLE مُضمّنًا أو مُرتبطًا كأيقونة في المستند. يسمح بتحديد ملف الأيقونة والتسمية التوضيحية. يكتشف نوع كائن OLE باستخدام مُعامل progID المُحدد.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, string progId, bool isLinked, string iconFile, 
    string iconCaption)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | المسار الكامل للملف. |
| progId | String | معرف برنامج كائن OLE. |
| isLinked | Boolean | إذا`حقيقي` ثم يتم إدراج كائن OLE المرتبط، وإلا يتم إدراج كائن OLE المضمن. |
| iconFile | String | المسار الكامل لملف ICO. إذا كانت القيمة`باطل` ، سوف يستخدم Aspose.Words صورة محددة مسبقًا. |
| iconCaption | String | عنوان الرمز. إذا كانت القيمة`باطل` سوف يستخدم Aspose.Words اسم الملف. |

### قيمة الإرجاع

عقدة الشكل التي تحتوي على كائن Ole والمدرجة في موضع المنشئ الحالي.

## أمثلة

يوضح كيفية إدراج كائن OLE مضمن أو مرتبط كأيقونة في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا تم حذف 'iconFile' و'iconCaption'، فإن هذه الطريقة المحملة تختار
// الرمز وفقًا لـ 'progId' ويستخدم اسم الملف لعنوان الرمز.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // إذا تم حذف 'iconFile' و'iconCaption'، فإن هذه الطريقة المحملة تختار
    // الرمز وفقًا لامتداد الملف ويستخدم اسم الملف لعنوان الرمز.
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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(*Stream, string, string, string*) {#insertoleobjectasicon}

يُدرج كائن OLE مُضمّن كأيقونة من دفق إلى المستند. يسمح بتحديد ملف الأيقونة والتسمية التوضيحية. يكتشف نوع كائن OLE باستخدام مُعامل progID المُعطى.

```csharp
public Shape InsertOleObjectAsIcon(Stream stream, string progId, string iconFile, 
    string iconCaption)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | تيار يحتوي على بيانات التطبيق. |
| progId | String | معرف برنامج كائن OLE. |
| iconFile | String | المسار الكامل لملف ICO. إذا كانت القيمة`باطل` ، سوف يستخدم Aspose.Words صورة محددة مسبقًا. |
| iconCaption | String | عنوان الرمز. إذا كانت القيمة`باطل` ، سوف يستخدم Aspose.Words رمز التسمية التوضيحية المحدد مسبقًا. |

### قيمة الإرجاع

عقدة الشكل التي تحتوي على كائن Ole والمدرجة في موضع المنشئ الحالي.

## أمثلة

يوضح كيفية إدراج كائن OLE مضمن أو مرتبط كأيقونة في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا تم حذف 'iconFile' و'iconCaption'، فإن هذه الطريقة المحملة تختار
// الرمز وفقًا لـ 'progId' ويستخدم اسم الملف لعنوان الرمز.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // إذا تم حذف 'iconFile' و'iconCaption'، فإن هذه الطريقة المحملة تختار
    // الرمز وفقًا لامتداد الملف ويستخدم اسم الملف لعنوان الرمز.
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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
