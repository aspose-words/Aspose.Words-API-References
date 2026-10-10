---
title: "طريقة Aspose::Words::DocumentBase::get_FootnoteSeparators"
linktitle: "get_FootnoteSeparators"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBase::get_FootnoteSeparators. توفر إمكانية الوصول إلى فواصل الحواشي/الحواشي السفلية المعرفة في المستند في C++."
type: docs
weight: 4500
url: /ar/cpp/aspose.words/documentbase/get_footnoteseparators/
---
## DocumentBase::get_FootnoteSeparators method


يوفر الوصول إلى فواصل الحواشي السفلية/الختامية المعرفة في المستند.

```cpp
System::SharedPtr<Aspose::Words::Notes::FootnoteSeparatorCollection> Aspose::Words::DocumentBase::get_FootnoteSeparators() const
```


## أمثلة



يعرض كيفية إزالة فاصل الحاشية الختامية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> endnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::EndnoteSeparator);
// إزالة فاصل الحاشية الختامية.
endnoteSeparator->get_FirstParagraph()->get_FirstChild()->Remove();
```


يظهر كيفية إدارة تنسيق فاصل الحاشية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// محاذاة فاصل الحاشية.
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## انظر أيضًا

* Class [FootnoteSeparatorCollection](../../../aspose.words.notes/footnoteseparatorcollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
