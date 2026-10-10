---
title: "Aspose::Words::DocumentBuilder::InsertFootnote طريقة"
linktitle: "InsertFootnote"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentBuilder::InsertFootnote طريقة. يدرج حاشية سفلية أو حاشية نهائية في المستند في C++."
type: docs
weight: 35000
url: /ar/cpp/aspose.words/documentbuilder/insertfootnote/
---
## DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType, const System::String\&) method


يدرج حاشية سفلية أو حاشية نهائية في المستند.

```cpp
System::SharedPtr<Aspose::Words::Notes::Footnote> Aspose::Words::DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType footnoteType, const System::String &footnoteText)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| footnoteType | Aspose::Words::Notes::FootnoteType | يحدد ما إذا كان سيتم إدراج حاشية سفلية أو حاشية نهائية. |
| footnoteText | const System::String\& | يحدد نص الحاشية السفلية. |

### ReturnValue

يرجع كائن حاشية سفلية تم إنشاؤه للتو.

## أمثلة



يوضح كيفية الإشارة إلى النص باستخدام حاشية سفلية وحاشية نهائية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج بعض النصوص وضع علامة عليها بحاشية سفلية مع ضبط الخاصية IsAuto إلى "true" بشكل افتراضي،
// بحيث سيتم ترقيم العلامة التي تُرى في نص الجسم تلقائيًا إلى "1",
// وستظهر الحاشية السفلية في أسفل الصفحة.
builder->Write(u"This text will be referenced by a footnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote comment regarding referenced text.");

// أدرج نصًا إضافيًا وضع علامة عليه بحاشية نهائية مع علامة إشارة مخصصة،
// والتي ستُستَخدم بدلًا من الرقم "2" وتضبط "IsAuto" إلى false.
builder->Write(u"This text will be referenced by an endnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote comment regarding referenced text.", u"CustomMark");

// الحواشي السفلية تظهر دائمًا في أسفل النص المُشار إليه،
// وبالتالي فإن فاصل الصفحة هذا لن يؤثر على الحاشية السفلية.
// من ناحية أخرى، الحواشي النهائية تكون دائمًا في نهاية المستند
// وبذلك سيؤدي فاصل الصفحة هذا إلى دفع الحاشية النهائية إلى الصفحة التالية.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFootnote.docx");
```

## انظر أيضًا

* Class [Footnote](../../../aspose.words.notes/footnote/)
* Enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType, const System::String\&, const System::String\&) method


يدرج حاشية سفلية أو حاشية نهائية في المستند.

```cpp
System::SharedPtr<Aspose::Words::Notes::Footnote> Aspose::Words::DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType footnoteType, const System::String &footnoteText, const System::String &referenceMark)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| footnoteType | Aspose::Words::Notes::FootnoteType | يحدد ما إذا كان سيتم إدراج حاشية سفلية أو حاشية نهائية. |
| footnoteText | const System::String\& | يحدد نص الحاشية السفلية. |
| referenceMark | const System::String\& | يحدد علامة الإشارة المخصصة للحاشية السفلية. |

### ReturnValue

يرجع كائن حاشية سفلية تم إنشاؤه للتو.

## أمثلة



يوضح كيفية الإشارة إلى النص باستخدام حاشية سفلية وحاشية نهائية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج بعض النصوص وضع علامة عليها بحاشية سفلية مع ضبط الخاصية IsAuto إلى "true" بشكل افتراضي،
// بحيث سيتم ترقيم العلامة التي تُرى في نص الجسم تلقائيًا إلى "1",
// وستظهر الحاشية السفلية في أسفل الصفحة.
builder->Write(u"This text will be referenced by a footnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote comment regarding referenced text.");

// أدرج نصًا إضافيًا وضع علامة عليه بحاشية نهائية مع علامة إشارة مخصصة،
// والتي ستُستَخدم بدلًا من الرقم "2" وتضبط "IsAuto" إلى false.
builder->Write(u"This text will be referenced by an endnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote comment regarding referenced text.", u"CustomMark");

// الحواشي السفلية تظهر دائمًا في أسفل النص المُشار إليه،
// وبالتالي فإن فاصل الصفحة هذا لن يؤثر على الحاشية السفلية.
// من ناحية أخرى، الحواشي النهائية تكون دائمًا في نهاية المستند
// وبذلك سيؤدي فاصل الصفحة هذا إلى دفع الحاشية النهائية إلى الصفحة التالية.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFootnote.docx");
```

## انظر أيضًا

* Class [Footnote](../../../aspose.words.notes/footnote/)
* Enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
