---
title: OleFormat.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية OleFormat SourceFullName، وقم بإدارة المسار واسم ملف المصدر الخاص بكائن OLE المرتبط بسهولة لتحقيق التكامل السلس.
type: docs
weight: 100
url: /ar/net/aspose.words.drawing/oleformat/sourcefullname/
---
## OleFormat.SourceFullName property

يحصل على مسار واسم ملف المصدر لكائن OLE المرتبط أو يعينه.

```csharp
public string SourceFullName { get; set; }
```

## ملاحظات

القيمة الافتراضية هي سلسلة فارغة.

لو`SourceFullName` ليس سلسلة فارغة، كائن OLE مرتبط.

## أمثلة

يوضح كيفية إدراج كائنات OLE المرتبطة وغير المرتبطة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تضمين رسم Microsoft Visio في المستند ككائن OLE.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", false, false, null);

// أدخل رابطًا للملف في نظام الملفات المحلي واعرضه كأيقونة.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", true, true, null);

// يؤدي إدراج كائنات OLE إلى إنشاء أشكال لتخزين هذه الكائنات.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);
Assert.AreEqual(2, shapes.Count(s => s.ShapeType == ShapeType.OleObject));

// إذا كان الشكل يحتوي على كائن OLE، فسيكون له خاصية "OleFormat" صالحة،
// والتي يمكننا استخدامها للتحقق من بعض جوانب الشكل.
OleFormat oleFormat = shapes[0].OleFormat;

Assert.AreEqual(false, oleFormat.IsLink);
Assert.AreEqual(false, oleFormat.OleIcon);

oleFormat = shapes[1].OleFormat;

Assert.AreEqual(true, oleFormat.IsLink);
Assert.AreEqual(true, oleFormat.OleIcon);

Assert.True(oleFormat.SourceFullName.EndsWith(@"Images" + Path.DirectorySeparatorChar + "Microsoft Visio drawing.vsd"));
Assert.AreEqual("", oleFormat.SourceItem);

Assert.AreEqual("Microsoft Visio drawing.vsd", oleFormat.IconCaption);

doc.Save(ArtifactsDir + "Shape.OleLinks.docx");

// إذا كان الكائن يحتوي على بيانات OLE، فيمكننا الوصول إليها باستخدام دفق.
using (MemoryStream stream = oleFormat.GetOleEntry("\x0001CompObj"))
{
    byte[] oleEntryBytes = stream.ToArray();
    Assert.AreEqual(76, oleEntryBytes.Length);
}
```

### أنظر أيضا

* class [OleFormat](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
