---
title: "فئة Aspose::Words::Drawing::OleFormat"
linktitle: "OleFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Drawing::OleFormat. توفر الوصول إلى بيانات كائن OLE أو عنصر تحكم ActiveX. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.drawing/oleformat/
---
## OleFormat class


يوفر إمكانية الوصول إلى بيانات كائن OLE أو عنصر تحكم ActiveX. لمعرفة المزيد، زر مقالة الوثائق [Working with Ole Objects](https://docs.aspose.com/words/cpp/working-with-ole-objects/).

```cpp
class OleFormat : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_AutoUpdate](./get_autoupdate/)() | يحدد ما إذا كان الارتباط بكائن OLE يتم تحديثه تلقائيًا أم لا في Microsoft Word. |
| [get_Clsid](./get_clsid/)() | يحصل على CLSID لكائن OLE. |
| [get_IconCaption](./get_iconcaption/)() | يحصل على تسمية أيقونة كائن OLE. في حال عدم وجود أيقونة لكائن OLE أو عدم إمكانية استرجاع التسمية، يُرجع سلسلة فارغة. |
| [get_IsLink](./get_islink/)() | يُرجع **true** إذا كان كائن OLE مرتبطًا (عند تحديد [SourceFullName](./get_sourcefullname/)). |
| [get_IsLocked](./get_islocked/)() | يحدد ما إذا كان الارتباط بكائن OLE مقفلًا من التحديثات. |
| [get_OleControl](./get_olecontrol/)() | يحصل على كائنات [OleControl](./get_olecontrol/) إذا كان كائن OLE هذا عنصر تحكم ActiveX. وإلا فإن هذه الخاصية تكون null. |
| [get_OleIcon](./get_oleicon/)() | يحصل على مظهر الرسم لكائن OLE. عندما **true**، يُعرض كائن OLE كأيقونة. عندما **false**، يُعرض كائن OLE كمحتوى. |
| [get_OlePackage](./get_olepackage/)() | يوفر الوصول إلى [OlePackage](../olepackage/) إذا كان كائن OLE حزمة OLE. يُرجع **null** خلاف ذلك. |
| [get_ProgId](./get_progid/)() | يحصل أو يعيّن ProgID لكائن OLE. |
| [get_SourceFullName](./get_sourcefullname/)() | يحصل أو يعيّن المسار والاسم لملف المصدر لكائن OLE المرتبط. |
| [get_SourceItem](./get_sourceitem/)() | يحصل أو يعيّن سلسلة تُستخدم لتحديد الجزء من ملف المصدر الذي يتم ربطه. |
| [get_SuggestedExtension](./get_suggestedextension/)() | يحصل على امتداد الملف المقترح للكائن المضمن الحالي إذا رغبت في حفظه في ملف. |
| [get_SuggestedFileName](./get_suggestedfilename/)() | يحصل على اسم الملف المقترح للكائن المضمن الحالي إذا رغبت في حفظه في ملف. |
| [GetOleEntry](./getoleentry/)(const System::String\&) | يحصل على مدخل بيانات كائن OLE. |
| [GetRawData](./getrawdata/)() | يحصل على البيانات الخام لكائن OLE. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | يحفظ بيانات الكائن المضمّن في الدفق المحدد. |
| [Save](./save/)(const System::String\&) | يحفظ بيانات الكائن المضمّن في ملف بالاسم المحدد. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_AutoUpdate](./set_autoupdate/)(bool) | محدد لـ [Aspose::Words::Drawing::OleFormat::get_AutoUpdate](./get_autoupdate/). |
| [set_IsLocked](./set_islocked/)(bool) | محدد لـ [Aspose::Words::Drawing::OleFormat::get_IsLocked](./get_islocked/). |
| [set_ProgId](./set_progid/)(const System::String\&) | محدد لـ [Aspose::Words::Drawing::OleFormat::get_ProgId](./get_progid/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | محدد لـ [Aspose::Words::Drawing::OleFormat::get_SourceFullName](./get_sourcefullname/). |
| [set_SourceItem](./set_sourceitem/)(const System::String\&) | محدد لـ [Aspose::Words::Drawing::OleFormat::get_SourceItem](./get_sourceitem/). |
| static [Type](./type/)() |  |
## ملاحظات


استخدم الخاصية [OleFormat](../shape/get_oleformat/) للوصول إلى بيانات كائن OLE. لا تقوم بإنشاء مثيلات من الفئة [OleFormat](./) مباشرة.

## أمثلة



يظهر كيفية استخراج كائنات OLE المضمّنة إلى ملفات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE spreadsheet.docm");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// كائن OLE في الشكل الأول هو جدول بيانات Microsoft Excel.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shape->get_OleFormat();

ASSERT_EQ(u"Excel.Sheet.12", oleFormat->get_ProgId());

// كائننا ليس محدثًا تلقائيًا ولا مقفلًا من التحديثات.
ASSERT_FALSE(oleFormat->get_AutoUpdate());
ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLocked());

// إذا كنا نخطط لحفظ كائن OLE إلى ملف في نظام الملفات المحلي،
// يمكننا استخدام الخاصية "SuggestedExtension" لتحديد امتداد الملف الذي يجب تطبيقه.
ASSERT_EQ(u".xlsx", oleFormat->get_SuggestedExtension());

// فيما يلي طريقتان لحفظ كائن OLE إلى ملف في نظام الملفات المحلي.
// 1 -  احفظه عبر دفق:
{
    auto fs = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"OLE spreadsheet extracted via stream" + oleFormat->get_SuggestedExtension(), System::IO::FileMode::Create);
    oleFormat->Save(fs);
}

// 2 -  احفظه مباشرةً إلى اسم ملف:
oleFormat->Save(get_ArtifactsDir() + u"OLE spreadsheet saved directly" + oleFormat->get_SuggestedExtension());
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
