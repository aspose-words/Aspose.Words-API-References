---
title: "Aspose::Words::ParagraphCollection::ToArray طريقة"
linktitle: "ToArray"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ParagraphCollection::ToArray طريقة. ينسخ جميع الفقرات من المجموعة إلى مصفوفة جديدة من الفقرات في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words/paragraphcollection/toarray/
---
## ParagraphCollection::ToArray method


ينسخ جميع الفقرات من المجموعة إلى مصفوفة جديدة من الفقرات.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Paragraph>> Aspose::Words::ParagraphCollection::ToArray()
```


### ReturnValue

مصفوفة من الفقرات.

## أمثلة



يظهر كيفية إنشاء مصفوفة من [NodeCollection](../../nodecollection/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Paragraph>> paras = doc->get_FirstSection()->get_Body()->get_Paragraphs()->ToArray();

ASSERT_EQ(22, paras->get_Length());
```


يظهر كيفية استخدام "hot remove" لإزالة عقدة أثناء التعداد.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"The first paragraph");
builder->Writeln(u"The second paragraph");
builder->Writeln(u"The third paragraph");
builder->Writeln(u"The fourth paragraph");

// إزالة عقدة من المجموعة في وسط عملية التعداد.
for (System::SharedPtr<Aspose::Words::Paragraph> para : doc->get_FirstSection()->get_Body()->get_Paragraphs()->ToArray())
{
    if (para->get_Range()->get_Text().Contains(u"third"))
    {
        para->Remove();
    }
}

ASSERT_FALSE(doc->GetText().Contains(u"The third paragraph"));
```

## انظر أيضًا

* Class [Paragraph](../../paragraph/)
* Class [ParagraphCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
