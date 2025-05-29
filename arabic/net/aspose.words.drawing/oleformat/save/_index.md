---
title: OleFormat.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة حفظ OleFormat لتخزين بيانات الكائنات المضمنة بكفاءة في المسار الذي تختاره. حسّن إدارة البيانات بسهولة!
type: docs
weight: 160
url: /ar/net/aspose.words.drawing/oleformat/save/
---
## Save(*Stream*) {#save}

يحفظ بيانات الكائن المضمن في التدفق المحدد.

```csharp
public void Save(Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | أين يتم حفظ بيانات الكائن؟ |

### استثناءات

| استثناء | حالة |
| --- | --- |
| InvalidOperationException | يتم رميه إذا حاولت حفظ كائن مرتبط. |

## ملاحظات

تقع على عاتق المتصل مسؤولية التخلص من التدفق.

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

---

## Save(*string*) {#save_1}

يحفظ بيانات الكائن المضمن في ملف يحمل الاسم المحدد.

```csharp
public void Save(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم الملف لحفظ بيانات كائن OLE. |

### استثناءات

| استثناء | حالة |
| --- | --- |
| InvalidOperationException | يتم رميه إذا حاولت حفظ كائن مرتبط. |

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
