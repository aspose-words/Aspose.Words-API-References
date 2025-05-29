---
title: OleFormat.SourceItem
linktitle: SourceItem
articleTitle: SourceItem
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية OleFormat SourceItem، وتعرف بسهولة على الأجزاء المرتبطة بملف المصدر الخاص بك وقم بإدارتها باستخدام وظيفة السلسلة الأساسية هذه.
type: docs
weight: 110
url: /ar/net/aspose.words.drawing/oleformat/sourceitem/
---
## OleFormat.SourceItem property

يحصل على سلسلة أو يعينها، والتي تُستخدم لتحديد جزء ملف المصدر الذي يتم ربطه.

```csharp
public string SourceItem { get; set; }
```

## ملاحظات

القيمة الافتراضية هي سلسلة فارغة.

على سبيل المثال، إذا كان ملف المصدر عبارة عن مصنف Microsoft Excel،`SourceItem` قد تقوم الخاصية بإرجاع "Workbook1!R3C1:R4C2" إذا كان كائن OLE يحتوي فقط على عدد قليل من الخلايا من ورقة العمل.

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
