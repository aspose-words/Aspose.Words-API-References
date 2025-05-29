---
title: OleFormat.ProgId
linktitle: ProgId
articleTitle: ProgId
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية OleFormat ProgId لإدارة وتخصيص معرفات كائنات OLE بسهولة لتحسين الوظائف والتكامل السلس.
type: docs
weight: 90
url: /ar/net/aspose.words.drawing/oleformat/progid/
---
## OleFormat.ProgId property

يحصل على ProgID الخاص بكائن OLE أو يعينه.

```csharp
public string ProgId { get; set; }
```

## ملاحظات

لا تتواجد خاصية ProgID دائمًا في مستندات Microsoft Word ولا يمكن الاعتماد عليها.

لا يمكن أن يكون`باطل`.

القيمة الافتراضية هي سلسلة فارغة.

## أمثلة

يوضح كيفية استخراج كائنات OLE المضمنة في الملفات.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// كائن OLE في الشكل الأول هو جدول بيانات Microsoft Excel.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// هدفنا ليس تحديثًا تلقائيًا ولا محظورًا من التحديثات.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// إذا كنا نخطط لحفظ كائن OLE في ملف في نظام الملفات المحلي،
// يمكننا استخدام الخاصية "SuggestedExtension" لتحديد امتداد الملف الذي سيتم تطبيقه على الملف.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// فيما يلي طريقتان لحفظ كائن OLE في ملف في نظام الملفات المحلي.
// 1 - احفظه عبر مجرى:
using (FileStream fs = new FileStream(ArtifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.SuggestedExtension, FileMode.Create))
{
    oleFormat.Save(fs);
}

// 2 - احفظه مباشرة في اسم الملف:
oleFormat.Save(ArtifactsDir + "OLE spreadsheet saved directly" + oleFormat.SuggestedExtension);
```

### أنظر أيضا

* class [OleFormat](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
