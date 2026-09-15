---
title: "طريقة Aspose::Words::Drawing::OleFormat::get_OleIcon"
linktitle: "get_OleIcon"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::OleFormat::get_OleIcon. يحصل على جانب الرسم لكائن OLE. عندما تكون true، يُعرض كائن OLE كأيقونة. عندما تكون false، يُعرض كائن OLE كمحتوى في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.drawing/oleformat/get_oleicon/
---
## OleFormat::get_OleIcon method


يحصل على مظهر الرسم لكائن OLE. عندما **true**، يُعرض كائن OLE كأيقونة. عندما **false**، يُعرض كائن OLE كمحتوى.

```cpp
bool Aspose::Words::Drawing::OleFormat::get_OleIcon()
```

## ملاحظات


لا يسمح Aspose.Words بتعيين هذه الخاصية لتجنب الالتباس. إذا كنت قادرًا على تغيير جانب الرسم في Aspose.Words، سيظل Microsoft Word يعرض كائن OLE في جانب الرسم الأصلي حتى تقوم بتحرير أو تحديث كائن OLE في Microsoft Word.

## أمثلة



يظهر كيفية إدراج كائنات OLE المرتبطة وغير المرتبطة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// تضمين رسم Microsoft Visio في المستند ككائن OLE.
builder->InsertOleObject(get_ImageDir() + u"Microsoft Visio drawing.vsd", u"Package", false, false, nullptr);

// إدراج ارتباط إلى الملف في نظام الملفات المحلي وعرضه كأيقونة.
builder->InsertOleObject(get_ImageDir() + u"Microsoft Visio drawing.vsd", u"Package", true, true, nullptr);

// إدراج كائنات OLE ينشئ أشكالًا تخزن هذه الكائنات.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());
ASSERT_EQ(2, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::OleObject;
}))));

// إذا كان الشكل يحتوي على كائن OLE، فسيكون لديه خاصية "OleFormat" صالحة،
// ويمكننا استخدامها للتحقق من بعض جوانب الشكل.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shapes[0]->get_OleFormat();

ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLink());
ASPOSE_ASSERT_EQ(false, oleFormat->get_OleIcon());

oleFormat = shapes[1]->get_OleFormat();

ASPOSE_ASSERT_EQ(true, oleFormat->get_IsLink());
ASPOSE_ASSERT_EQ(true, oleFormat->get_OleIcon());

ASSERT_TRUE(oleFormat->get_SourceFullName().EndsWith(System::String(u"Images") + System::IO::Path::DirectorySeparatorChar + u"Microsoft Visio drawing.vsd"));
ASSERT_EQ(u"", oleFormat->get_SourceItem());

ASSERT_EQ(u"Microsoft Visio drawing.vsd", oleFormat->get_IconCaption());

doc->Save(get_ArtifactsDir() + u"Shape.OleLinks.docx");

// إذا كان الكائن يحتوي على بيانات OLE، يمكننا الوصول إليها باستخدام تدفق.
{
    System::SharedPtr<System::IO::MemoryStream> stream = oleFormat->GetOleEntry(u"\x0001" u"CompObj");
    System::ArrayPtr<uint8_t> oleEntryBytes = stream->ToArray();
    ASSERT_EQ(76, oleEntryBytes->get_Length());
}
```

## انظر أيضًا

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
