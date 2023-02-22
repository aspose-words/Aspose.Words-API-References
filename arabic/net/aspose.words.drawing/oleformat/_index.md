---
title: Class OleFormat
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.OleFormat فصل. يوفر الوصول إلى بيانات كائن OLE أو عنصر تحكم ActiveX.
type: docs
weight: 1020
url: /ar/net/aspose.words.drawing/oleformat/
---
## OleFormat class

يوفر الوصول إلى بيانات كائن OLE أو عنصر تحكم ActiveX.

```csharp
public class OleFormat
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [AutoUpdate](../../aspose.words.drawing/oleformat/autoupdate/) { get; set; } | يحدد ما إذا كان الارتباط إلى كائن OLE يتم تحديثه تلقائيًا أم لا في Microsoft Word. |
| [Clsid](../../aspose.words.drawing/oleformat/clsid/) { get; } | الحصول على CLSID الخاص بكائن OLE. |
| [IconCaption](../../aspose.words.drawing/oleformat/iconcaption/) { get; } | الحصول على رمز التسمية التوضيحية لكائن OLE . |
| [IsLink](../../aspose.words.drawing/oleformat/islink/) { get; } | إرجاع صحيح إذا تم ربط كائن OLE (عندما[`SourceFullName`](./sourcefullname/) محدد) . |
| [IsLocked](../../aspose.words.drawing/oleformat/islocked/) { get; set; } | يحدد ما إذا كان الارتباط بكائن OLE مؤمنًا من التحديثات. |
| [OleControl](../../aspose.words.drawing/oleformat/olecontrol/) { get; } | يحصل[`OleControl`](./olecontrol/) كائنات إذا كان كائن OLE هذا عنصر تحكم ActiveX. وإلا فإن هذه الخاصية لاغية. |
| [OleIcon](../../aspose.words.drawing/oleformat/oleicon/) { get; } | الحصول على وجه الرسم لكائن OLE. متي **حقيقي** ، يتم عرض كائن OLE كرمز. متى **خاطئة** ، يتم عرض كائن OLE كمحتوى. |
| [OlePackage](../../aspose.words.drawing/oleformat/olepackage/) { get; } | توفير الوصول إلى[`OlePackage`](../olepackage/) إذا كان كائن OLE عبارة عن حزمة OLE. إرجاع فارغ وإلا . |
| [ProgId](../../aspose.words.drawing/oleformat/progid/) { get; set; } | الحصول على أو تعيين ProgID الخاص بكائن OLE. |
| [SourceFullName](../../aspose.words.drawing/oleformat/sourcefullname/) { get; set; } | الحصول على أو تعيين مسار واسم الملف المصدر لكائن OLE المرتبط. |
| [SourceItem](../../aspose.words.drawing/oleformat/sourceitem/) { get; set; } | الحصول على أو تعيين سلسلة يتم استخدامها لتعريف جزء الملف المصدر الذي يتم ربطه. |
| [SuggestedExtension](../../aspose.words.drawing/oleformat/suggestedextension/) { get; } | يحصل على امتداد الملف المقترح للكائن المضمن الحالي إذا كنت تريد حفظه في ملف. |
| [SuggestedFileName](../../aspose.words.drawing/oleformat/suggestedfilename/) { get; } | يحصل على اسم الملف المقترح للكائن المضمن الحالي إذا كنت تريد حفظه في ملف. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetOleEntry](../../aspose.words.drawing/oleformat/getoleentry/)(string) | يحصل على إدخال بيانات كائن OLE . |
| [GetRawData](../../aspose.words.drawing/oleformat/getrawdata/)() | الحصول على بيانات أولية لكائن OLE . |
| [Save](../../aspose.words.drawing/oleformat/save/#save)(Stream) | يحفظ بيانات الكائن المضمن في الدفق المحدد. |
| [Save](../../aspose.words.drawing/oleformat/save/#save_1)(string) | يحفظ بيانات الكائن المضمن في ملف بالاسم المحدد. |

### ملاحظات

استخدم ال[`OleFormat`](../shape/oleformat/) الخاصية للوصول إلى بيانات كائن OLE . لا يمكنك إنشاء مثيلات من`OleFormat` فئة مباشرة.

### أمثلة

يوضح كيفية استخراج كائنات OLE المضمنة في الملفات.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// كائن OLE في الشكل الأول هو جدول بيانات Microsoft Excel.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// كائننا لا يتم تحديثه تلقائيًا ولا يتم قفله من التحديثات.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// إذا كنا نخطط لحفظ كائن OLE في ملف في نظام الملفات المحلي ،
// يمكننا استخدام خاصية "اقتراح ملحق" لتحديد امتداد الملف المطلوب تطبيقه على الملف.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// فيما يلي طريقتان لحفظ كائن OLE إلى ملف في نظام الملفات المحلي.
// 1 - احفظه عبر تيار:
using (FileStream fs = new FileStream(ArtifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.SuggestedExtension, FileMode.Create))
{
    oleFormat.Save(fs);
}

// 2 - احفظه مباشرة في اسم ملف:
oleFormat.Save(ArtifactsDir + "OLE spreadsheet saved directly" + oleFormat.SuggestedExtension);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)


