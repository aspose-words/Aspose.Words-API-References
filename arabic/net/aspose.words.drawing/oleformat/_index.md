---
title: OleFormat Class
linktitle: OleFormat
articleTitle: OleFormat
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.OleFormat فصل. يوفر الوصول إلى بيانات كائن OLE أو عنصر تحكم ActiveX في C#.
type: docs
weight: 1150
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
| [AutoUpdate](../../aspose.words.drawing/oleformat/autoupdate/) { get; set; } | يحدد ما إذا كان الارتباط بكائن OLE سيتم تحديثه تلقائيًا أم لا في Microsoft Word. |
| [Clsid](../../aspose.words.drawing/oleformat/clsid/) { get; } | الحصول على CLSID لكائن OLE. |
| [IconCaption](../../aspose.words.drawing/oleformat/iconcaption/) { get; } | الحصول على تسمية توضيحية لكائن OLE. |
| [IsLink](../../aspose.words.drawing/oleformat/islink/) { get; } | إرجاع`حقيقي` إذا كان كائن OLE مرتبطًا (متى[`SourceFullName`](./sourcefullname/) تم تحديده). |
| [IsLocked](../../aspose.words.drawing/oleformat/islocked/) { get; set; } | يحدد ما إذا كان الارتباط بكائن OLE مؤمنًا من التحديثات. |
| [OleControl](../../aspose.words.drawing/oleformat/olecontrol/) { get; } | يحصل[`OleControl`](./olecontrol/) الكائنات إذا كان كائن OLE هذا هو عنصر تحكم ActiveX. وإلا فإن هذه الخاصية فارغة. |
| [OleIcon](../../aspose.words.drawing/oleformat/oleicon/) { get; } | الحصول على مظهر الرسم لكائن OLE. متى`حقيقي` ، يتم عرض كائن OLE كرمز. متى`خطأ شنيع` ، يتم عرض كائن OLE كمحتوى. |
| [OlePackage](../../aspose.words.drawing/oleformat/olepackage/) { get; } | توفير الوصول إلى[`OlePackage`](../olepackage/) إذا كان كائن OLE عبارة عن حزمة OLE. Returns`باطل` وإلا. |
| [ProgId](../../aspose.words.drawing/oleformat/progid/) { get; set; } | الحصول على ProgID لكائن OLE أو تعيينه. |
| [SourceFullName](../../aspose.words.drawing/oleformat/sourcefullname/) { get; set; } | الحصول على أو تعيين مسار واسم الملف المصدر لكائن OLE المرتبط. |
| [SourceItem](../../aspose.words.drawing/oleformat/sourceitem/) { get; set; } | الحصول على أو تعيين سلسلة يتم استخدامها لتحديد جزء الملف المصدر الذي يتم ربطه. |
| [SuggestedExtension](../../aspose.words.drawing/oleformat/suggestedextension/) { get; } | احصل على امتداد الملف المقترح للكائن المضمن الحالي إذا كنت تريد حفظه في ملف. |
| [SuggestedFileName](../../aspose.words.drawing/oleformat/suggestedfilename/) { get; } | يحصل على اسم الملف المقترح للكائن المضمن الحالي إذا كنت تريد حفظه في ملف. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetOleEntry](../../aspose.words.drawing/oleformat/getoleentry/)(*string*) | يحصل على إدخال بيانات كائن OLE. |
| [GetRawData](../../aspose.words.drawing/oleformat/getrawdata/)() | يحصل على البيانات الأولية لكائن OLE. |
| [Save](../../aspose.words.drawing/oleformat/save/#save)(*Stream*) | يحفظ بيانات الكائن المضمن في الدفق المحدد. |
| [Save](../../aspose.words.drawing/oleformat/save/#save_1)(*string*) | يحفظ بيانات الكائن المضمن في ملف بالاسم المحدد. |

## ملاحظات

استخدم ال[`OleFormat`](../shape/oleformat/)الخاصية للوصول إلى بيانات كائن OLE. لا تقم بإنشاء مثيلات لـ`OleFormat` الصف مباشرة.

## أمثلة

يوضح كيفية استخراج كائنات OLE المضمنة في الملفات.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// كائن OLE الموجود في الشكل الأول هو جدول بيانات Microsoft Excel.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// كائننا لا يتم تحديثه تلقائيًا ولا يتم قفله من التحديثات.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// إذا كنا نخطط لحفظ كائن OLE في ملف في نظام الملفات المحلي،
// يمكننا استخدام خاصية "SuggestedExtension" لتحديد امتداد الملف الذي سيتم تطبيقه على الملف.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// فيما يلي طريقتان لحفظ كائن OLE في ملف في نظام الملفات المحلي.
// 1 - احفظه عبر الدفق:
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
