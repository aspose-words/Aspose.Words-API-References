---
title: OleFormat Class
linktitle: OleFormat
articleTitle: OleFormat
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.OleFormat للوصول بشكل سلس إلى كائنات OLE وعناصر التحكم ActiveX، مما يعزز قدرات معالجة المستندات لديك.
type: docs
weight: 1530
url: /ar/net/aspose.words.drawing/oleformat/
---
## OleFormat class

يوفر الوصول إلى بيانات كائن OLE أو عنصر تحكم ActiveX.

لمعرفة المزيد، قم بزيارة[العمل مع كائنات Ole](https://docs.aspose.com/words/net/working-with-ole-objects/) مقالة توثيقية.

```csharp
public class OleFormat
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [AutoUpdate](../../aspose.words.drawing/oleformat/autoupdate/) { get; set; } | يحدد ما إذا كان الارتباط بكائن OLE يتم تحديثه تلقائيًا أم لا في Microsoft Word. |
| [Clsid](../../aspose.words.drawing/oleformat/clsid/) { get; } | يحصل على CLSID لكائن OLE. |
| [IconCaption](../../aspose.words.drawing/oleformat/iconcaption/) { get; } | يحصل على تسمية توضيحية لأيقونة كائن OLE. |
| [IsLink](../../aspose.words.drawing/oleformat/islink/) { get; } | إرجاع`حقيقي` إذا تم ربط كائن OLE (عندما[`SourceFullName`](./sourcefullname/) (تم تحديده). |
| [IsLocked](../../aspose.words.drawing/oleformat/islocked/) { get; set; } | يحدد ما إذا كان الارتباط بكائن OLE مقفلاً ضد التحديثات. |
| [OleControl](../../aspose.words.drawing/oleformat/olecontrol/) { get; } | يحصل[`OleControl`](./olecontrol/) إذا كان كائن OLE هذا عنصر تحكم ActiveX. وإلا، تكون هذه الخاصية فارغة. |
| [OleIcon](../../aspose.words.drawing/oleformat/oleicon/) { get; } | يحصل على جانب الرسم لكائن OLE. عندما`حقيقي`، يتم عرض كائن OLE كأيقونة. عندما`خطأ شنيع` ، يتم عرض كائن OLE كمحتوى. |
| [OlePackage](../../aspose.words.drawing/oleformat/olepackage/) { get; } | توفير الوصول إلى[`OlePackage`](../olepackage/) إذا كان كائن OLE عبارة عن حزمة OLE. يتم إرجاعها`باطل` وإلا. |
| [ProgId](../../aspose.words.drawing/oleformat/progid/) { get; set; } | يحصل على ProgID الخاص بكائن OLE أو يعينه. |
| [SourceFullName](../../aspose.words.drawing/oleformat/sourcefullname/) { get; set; } | يحصل على مسار واسم ملف المصدر لكائن OLE المرتبط أو يعينه. |
| [SourceItem](../../aspose.words.drawing/oleformat/sourceitem/) { get; set; } | يحصل على سلسلة أو يعينها، والتي تُستخدم لتحديد جزء ملف المصدر الذي يتم ربطه. |
| [SuggestedExtension](../../aspose.words.drawing/oleformat/suggestedextension/) { get; } | يحصل على امتداد الملف المقترح للكائن المضمن الحالي إذا كنت تريد حفظه في ملف. |
| [SuggestedFileName](../../aspose.words.drawing/oleformat/suggestedfilename/) { get; } | يحصل على اسم الملف المقترح للكائن المضمن الحالي إذا كنت تريد حفظه في ملف. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetOleEntry](../../aspose.words.drawing/oleformat/getoleentry/)(*string*) | يحصل على إدخال بيانات كائن OLE. |
| [GetRawData](../../aspose.words.drawing/oleformat/getrawdata/)() | يحصل على بيانات خام لكائن OLE. |
| [Save](../../aspose.words.drawing/oleformat/save/#save)(*Stream*) | يحفظ بيانات الكائن المضمن في التدفق المحدد. |
| [Save](../../aspose.words.drawing/oleformat/save/#save_1)(*string*) | يحفظ بيانات الكائن المضمن في ملف يحمل الاسم المحدد. |

## ملاحظات

استخدم[`OleFormat`](../shape/oleformat/) الخاصية للوصول إلى بيانات كائن OLE. لا تقم بإنشاء مثيلات من`OleFormat` الصف مباشرة.

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

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
