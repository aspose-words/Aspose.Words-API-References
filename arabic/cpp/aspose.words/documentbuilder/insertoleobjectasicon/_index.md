---
title: "طريقة Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon"
linktitle: "InsertOleObjectAsIcon"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon. تُدرج كائن OLE مضمّن كأيقونة من تدفق بيانات إلى المستند. تسمح بتحديد ملف الأيقونة والتسمية التوضيحية. تُحدد نوع كائن OLE باستخدام معلمة progID المقدمة بلغة C++."
type: docs
weight: 42000
url: /ar/cpp/aspose.words/documentbuilder/insertoleobjectasicon/
---
## DocumentBuilder::InsertOleObjectAsIcon(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, const System::String\&, const System::String\&) method


يقوم بإدراج كائن OLE مدمج كأيقونة من تدفق بيانات في المستند. يسمح بتحديد ملف الأيقونة والتعليق. يكتشف نوع كائن OLE باستخدام معامل progID المقدم.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::SharedPtr<System::IO::Stream> &stream, const System::String &progId, const System::String &iconFile, const System::String &iconCaption)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| تدفق | const System::SharedPtr\<System::IO::Stream\>\& | تدفق يحتوي على بيانات التطبيق. |
| progId | const System::String\& | ProgId لكائن OLE. |
| iconFile | const System::String\& | المسار الكامل لملف ICO. إذا كانت القيمة **null**، سيستخدم Aspose.Words صورة معرفة مسبقًا. |
| iconCaption | const System::String\& | تسمية الأيقونة. إذا كانت القيمة **null**، سيستخدم Aspose.Words تسمية أيقونة معرفة مسبقًا. |

### ReturnValue

عقدة الشكل التي تحتوي على كائن Ole وتُدرج في موضع Builder الحالي.

## أمثلة



يظهر كيفية إدراج كائن OLE مضمّن أو مرتبط كأيقونة في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إذا تم حذف 'iconFile' و 'iconCaption'، فإن هذه الطريقة المحملة تختار
// الأيقونة وفقًا لـ 'progId' وتستخدم اسم الملف كتسمية للأيقونة.
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", u"Package", false, get_ImageDir() + u"Logo icon.ico", u"My embedded file");

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    // إذا تم حذف 'iconFile' و 'iconCaption'، فإن هذه الطريقة المحملة تختار
    // الأيقونة وفقًا لامتداد الملف وتستخدم اسم الملف كتسمية للأيقونة.
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObjectAsIcon(stream, u"PowerPoint.Application", get_ImageDir() + u"Logo icon.ico", u"My embedded file stream");

    System::SharedPtr<Aspose::Words::Drawing::OlePackage> setOlePackage = shape->get_OleFormat()->get_OlePackage();
    setOlePackage->set_FileName(u"Presentation.pptx");
    setOlePackage->set_DisplayName(u"Presentation.pptx");
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjectAsIcon.docx");
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObjectAsIcon(const System::String\&, bool, const System::String\&, const System::String\&) method


يقوم بإدراج كائن OLE مدمج أو مرتبط كأيقونة في المستند. يسمح بتحديد ملف الأيقونة والتعليق. يكتشف نوع كائن OLE باستخدام امتداد الملف.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::String &fileName, bool isLinked, const System::String &iconFile, const System::String &iconCaption)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fileName | const System::String\& | المسار الكامل للملف. |
| isLinked | bool | إذا كان **true** فسيتم إدراج كائن OLE مرتبط، وإلا سيتم إدراج كائن OLE مضمّن. |
| iconFile | const System::String\& | المسار الكامل لملف ICO. إذا كانت القيمة **null**، سيستخدم Aspose.Words صورة معرفة مسبقًا. |
| iconCaption | const System::String\& | تسمية الأيقونة. إذا كانت القيمة **null**، سيستخدم Aspose.Words اسم الملف. |

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
## DocumentBuilder::InsertOleObjectAsIcon(const System::String\&, const System::String\&, bool, const System::String\&, const System::String\&) method


يقوم بإدراج كائن OLE مدمج أو مرتبط كأيقونة في المستند. يسمح بتحديد ملف الأيقونة والتعليق. يكتشف نوع كائن OLE باستخدام معامل progID المقدم.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::String &fileName, const System::String &progId, bool isLinked, const System::String &iconFile, const System::String &iconCaption)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fileName | const System::String\& | المسار الكامل للملف. |
| progId | const System::String\& | ProgId لكائن OLE. |
| isLinked | bool | إذا كان **true** فسيتم إدراج كائن OLE مرتبط، وإلا سيتم إدراج كائن OLE مضمّن. |
| iconFile | const System::String\& | المسار الكامل لملف ICO. إذا كانت القيمة **null**، سيستخدم Aspose.Words صورة معرفة مسبقًا. |
| iconCaption | const System::String\& | تسمية الأيقونة. إذا كانت القيمة **null**، سيستخدم Aspose.Words اسم الملف. |

### ReturnValue

عقدة الشكل التي تحتوي على كائن Ole وتُدرج في موضع Builder الحالي.

## أمثلة



يظهر كيفية إدراج كائن OLE مضمّن أو مرتبط كأيقونة في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إذا تم حذف 'iconFile' و 'iconCaption'، فإن هذه الطريقة المحملة تختار
// الأيقونة وفقًا لـ 'progId' وتستخدم اسم الملف كتسمية للأيقونة.
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", u"Package", false, get_ImageDir() + u"Logo icon.ico", u"My embedded file");

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    // إذا تم حذف 'iconFile' و 'iconCaption'، فإن هذه الطريقة المحملة تختار
    // الأيقونة وفقًا لامتداد الملف وتستخدم اسم الملف كتسمية للأيقونة.
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObjectAsIcon(stream, u"PowerPoint.Application", get_ImageDir() + u"Logo icon.ico", u"My embedded file stream");

    System::SharedPtr<Aspose::Words::Drawing::OlePackage> setOlePackage = shape->get_OleFormat()->get_OlePackage();
    setOlePackage->set_FileName(u"Presentation.pptx");
    setOlePackage->set_DisplayName(u"Presentation.pptx");
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjectAsIcon.docx");
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObjectAsIcon(std::basic_istream\<CharType, Traits\>\&, System::String, System::String, System::String) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(std::basic_istream<CharType, Traits> &stream, System::String progId, System::String iconFile, System::String iconCaption)
```

## انظر أيضًا

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
