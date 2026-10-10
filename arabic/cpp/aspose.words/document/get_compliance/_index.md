---
title: "طريقة Aspose::Words::Document::get_Compliance"
linktitle: "get_Compliance"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::get_Compliance. تحصل على نسخة التوافق OOXML المحددة من محتوى المستند المحمَّل. لا يكون ذا معنى إلا للمستندات OOXML في C++."
type: docs
weight: 17000
url: /ar/cpp/aspose.words/document/get_compliance/
---
## Document::get_Compliance method


يحصل على نسخة توافق OOXML المحددة من محتوى المستند المحمَّل. لا معنى لها إلا في مستندات OOXML.

```cpp
Aspose::Words::Saving::OoxmlCompliance Aspose::Words::Document::get_Compliance()
```

## ملاحظات


إذا أنشأت مستندًا فارغًا جديدًا أو حمَّلت مستندًا غير OOXML، فإنها تُعيد قيمة [Ecma376_2006](../../../aspose.words.saving/ooxmlcompliance/).

## أمثلة



يظهر كيفية قراءة نسخة توافق Open Office XML للمستند المحمَّل.
```cpp
// تختلف نسخة التوافق بين المستندات التي تم إنشاؤها بإصدارات مختلفة من Microsoft Word.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.doc");
ASSERT_EQ(doc->get_Compliance(), Aspose::Words::Saving::OoxmlCompliance::Ecma376_2006);

doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
ASSERT_EQ(doc->get_Compliance(), Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);
```

## انظر أيضًا

* Enum [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
