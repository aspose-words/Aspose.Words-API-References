---
title: "طريقة Aspose::Words::Drawing::OleFormat::Save"
linktitle: "Save"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::OleFormat::Save. يحفظ بيانات الكائن المضمن في الدفق المحدد في C++."
type: docs
weight: 19000
url: /ar/cpp/aspose.words.drawing/oleformat/save/
---
## OleFormat::Save(const System::SharedPtr\<System::IO::Stream\>\&) method


يحفظ بيانات الكائن المضمّن في الدفق المحدد.

```cpp
void Aspose::Words::Drawing::OleFormat::Save(const System::SharedPtr<System::IO::Stream> &stream)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| تدفق | const System::SharedPtr\<System::IO::Stream\>\& | أين يتم حفظ بيانات الكائن؟ |
## ملاحظات


إنها مسؤولية المستدعي تحرير الدفق.

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

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## OleFormat::Save(const System::String\&) method


يحفظ بيانات الكائن المضمّن في ملف بالاسم المحدد.

```cpp
void Aspose::Words::Drawing::OleFormat::Save(const System::String &fileName)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fileName | const System::String\& | اسم الملف لحفظ بيانات كائن OLE. |

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

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## OleFormat::Save(std::basic_ostream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Drawing::OleFormat::Save(std::basic_ostream<CharType, Traits> &stream)
```

## انظر أيضًا

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
