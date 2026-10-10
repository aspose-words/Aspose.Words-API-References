---
title: "Aspose::Words::DocumentBuilder::InsertOleObject method"
linktitle: "InsertOleObject"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentBuilder::InsertOleObject method. يُدرج كائن OLE مدمج من تدفق إلى المستند في C++."
type: docs
weight: 41000
url: /ar/cpp/aspose.words/documentbuilder/insertoleobject/
---
## DocumentBuilder::InsertOleObject(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


يقوم بإدراج كائن OLE مدمج من تدفق بيانات في المستند.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::SharedPtr<System::IO::Stream> &stream, const System::String &progId, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| تدفق | const System::SharedPtr\<System::IO::Stream\>\& | تدفق يحتوي على بيانات التطبيق. |
| progId | const System::String\& | المعرّف البرمجي لكائن OLE. |
| asIcon | bool | يحدد إما وضع أيقوني أو عادي لكائن OLE الذي يتم إدراجه. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | عرض صورة لكائن OLE. إذا كانت القيمة **null** فإن Aspose.Words سيستخدم إحدى الصور المعرفة مسبقًا. |

### ReturnValue

عقدة الشكل التي تحتوي على كائن Ole وتُدرج في موضع Builder الحالي.

## أمثلة



يوضح كيفية استخدام مُنشئ المستند لتضمين كائنات OLE في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إدراج جدول بيانات Microsoft Excel من نظام الملفات المحلي
// في المستند مع الحفاظ على مظهره الافتراضي.
{
    System::SharedPtr<System::IO::Stream> spreadsheetStream = System::IO::File::Open(get_MyDir() + u"Spreadsheet.xlsx", System::IO::FileMode::Open);
    builder->Writeln(u"Spreadsheet Ole object:");
    // إذا تم حذف 'presentation' وتم تعيين 'asIcon'، فإن هذه الطريقة المحملة تختار
    // الأيقونة وفقًا لـ 'progId' وتستخدم تسمية الأيقونة المعرفة مسبقًا.
    builder->InsertOleObject(spreadsheetStream, u"OleObject.xlsx", false, nullptr);
}

// إدراج عرض تقديمي Microsoft Powerpoint ككائن OLE.
// هذه المرة، سيحتوي على صورة تم تنزيلها من الويب كأيقونة.
{
    System::SharedPtr<System::IO::Stream> powerpointStream = System::IO::File::Open(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    System::ArrayPtr<uint8_t> imgBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

    {
        auto imageStream = System::MakeObject<System::IO::MemoryStream>(imgBytes);
        builder->InsertParagraph();
        builder->Writeln(u"Powerpoint Ole object:");
        builder->InsertOleObject(powerpointStream, u"OleObject.pptx", true, imageStream);
    }
}

// انقر نقرًا مزدوجًا على هذه الكائنات في Microsoft Word لفتحها
// الملفات المرتبطة باستخدام التطبيقات الخاصة بها.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjects.docx");
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


يقوم بإدراج كائن OLE مدمج أو مرتبط من ملف في المستند. يكتشف نوع كائن OLE باستخدام امتداد الملف.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::String &fileName, bool isLinked, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fileName | const System::String\& | المسار الكامل للملف. |
| isLinked | bool | إذا كان **true** فسيتم إدراج كائن OLE مرتبط، وإلا سيتم إدراج كائن OLE مضمّن. |
| asIcon | bool | يحدد إما وضع أيقوني أو عادي لكائن OLE الذي يتم إدراجه. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | عرض صورة لكائن OLE. إذا كانت القيمة **null** فإن Aspose.Words سيستخدم إحدى الصور المعرفة مسبقًا. |

### ReturnValue

عقدة الشكل التي تحتوي على كائن Ole وتُدرج في موضع Builder الحالي.

## أمثلة



يظهر كيفية إدراج كائن OLE في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// كائنات OLE هي روابط إلى ملفات في نظام الملفات المحلي لدينا يمكن فتحها بواسطة تطبيقات أخرى مثبتة.
// النقر المزدوج على هذه الأشكال سيطلق التطبيق، ثم يستخدمه لفتح الكائن المرتبط.
// هناك ثلاث طرق لاستخدام طريقة InsertOleObject لإدراج هذه الأشكال وتكوين مظهرها.
// 1 - صورة مأخوذة من نظام الملفات المحلي:
{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    // إذا تم حذف 'presentation' وتم تعيين 'asIcon'، فإن هذه الطريقة المحملة تختار
    // الأيقونة وفقًا لامتداد الملف وتستخدم اسم الملف كتسمية للأيقونة.
    builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", false, false, imageStream);
}

// إذا تم حذف 'presentation' وتم تعيين 'asIcon'، فإن هذه الطريقة المحملة تختار
// الأيقونة وفقًا لـ 'progId' وتستخدم اسم الملف كتسمية للأيقونة.
// 2 - أيقونة تعتمد على التطبيق الذي سيفتح الكائن:
builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", u"Excel.Sheet", false, true, nullptr);

// إذا تم حذف 'iconFile' و 'iconCaption'، فإن هذه الطريقة المحملة تختار
// الأيقونة وفقًا لـ 'progId' وتستخدم تسمية الأيقونة المعرفة مسبقًا.
// 3 - أيقونة صورة بحجم 32 × 32 بكسل أو أصغر من نظام الملفات المحلي، مع تسمية مخصصة:
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", false, get_ImageDir() + u"Logo icon.ico", u"Double click to view presentation!");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObject.docx");
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(const System::String\&, const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


يقوم بإدراج كائن OLE مدمج أو مرتبط من ملف في المستند. يكتشف نوع كائن OLE باستخدام معامل progID المقدم.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::String &fileName, const System::String &progId, bool isLinked, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fileName | const System::String\& | المسار الكامل للملف. |
| progId | const System::String\& | ProgId لكائن OLE. |
| isLinked | bool | إذا كان **true** فسيتم إدراج كائن OLE مرتبط، وإلا سيتم إدراج كائن OLE مضمّن. |
| asIcon | bool | يحدد إما وضع أيقوني أو عادي لكائن OLE الذي يتم إدراجه. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | عرض صورة لكائن OLE. إذا كانت القيمة **null** فإن Aspose.Words سيستخدم إحدى الصور المعرفة مسبقًا. |

### ReturnValue

عقدة الشكل التي تحتوي على كائن Ole وتُدرج في موضع Builder الحالي.

## أمثلة



يظهر كيفية إدراج كائن OLE في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// كائنات OLE هي روابط إلى ملفات في نظام الملفات المحلي لدينا يمكن فتحها بواسطة تطبيقات أخرى مثبتة.
// النقر المزدوج على هذه الأشكال سيطلق التطبيق، ثم يستخدمه لفتح الكائن المرتبط.
// هناك ثلاث طرق لاستخدام طريقة InsertOleObject لإدراج هذه الأشكال وتكوين مظهرها.
// 1 - صورة مأخوذة من نظام الملفات المحلي:
{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    // إذا تم حذف 'presentation' وتم تعيين 'asIcon'، فإن هذه الطريقة المحملة تختار
    // الأيقونة وفقًا لامتداد الملف وتستخدم اسم الملف كتسمية للأيقونة.
    builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", false, false, imageStream);
}

// إذا تم حذف 'presentation' وتم تعيين 'asIcon'، فإن هذه الطريقة المحملة تختار
// الأيقونة وفقًا لـ 'progId' وتستخدم اسم الملف كتسمية للأيقونة.
// 2 - أيقونة تعتمد على التطبيق الذي سيفتح الكائن:
builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", u"Excel.Sheet", false, true, nullptr);

// إذا تم حذف 'iconFile' و 'iconCaption'، فإن هذه الطريقة المحملة تختار
// الأيقونة وفقًا لـ 'progId' وتستخدم تسمية الأيقونة المعرفة مسبقًا.
// 3 - أيقونة صورة بحجم 32 × 32 بكسل أو أصغر من نظام الملفات المحلي، مع تسمية مخصصة:
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", false, get_ImageDir() + u"Logo icon.ico", u"Double click to view presentation!");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObject.docx");
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(std::basic_istream\<CharType, Traits\>\&, System::String, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(std::basic_istream<CharType, Traits> &stream, System::String progId, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(System::String fileName, bool isLinked, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(System::String, System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(System::String fileName, System::String progId, bool isLinked, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
