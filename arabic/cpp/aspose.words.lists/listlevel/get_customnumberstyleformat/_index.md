---
title: "طريقة Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat"
linktitle: "get_CustomNumberStyleFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat. تُحصل أو تُعيّن تنسيق نمط الرقم المخصص لهذا المستوى من القائمة. على سبيل المثال: \"a, ç, ĝ, ...\" في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.lists/listlevel/get_customnumberstyleformat/
---
## ListLevel::get_CustomNumberStyleFormat method


يحصل أو يضبط تنسيق نمط الرقم المخصص لهذا المستوى من القائمة. على سبيل المثال: "a, ç, ĝ, ...".

```cpp
System::String Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat()
```


## أمثلة



يُظهر كيفية الحصول على التنسيق لقائمة ذات نمط رقم مخصص.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with leading zero.docx");

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ListFormat()->get_ListLevel();

System::String customNumberStyleFormat = System::String::Empty;

if (listLevel->get_NumberStyle() == Aspose::Words::NumberStyle::Custom)
{
    customNumberStyleFormat = listLevel->get_CustomNumberStyleFormat();
}

ASSERT_EQ(u"001, 002, 003, ...", customNumberStyleFormat);

// يمكننا الحصول على القيمة للفهرس المحدد لعنصر القائمة.
ASSERT_EQ(u"iv", Aspose::Words::Lists::ListLevel::GetEffectiveValue(4, Aspose::Words::NumberStyle::LowercaseRoman, nullptr));
ASSERT_EQ(u"005", Aspose::Words::Lists::ListLevel::GetEffectiveValue(5, Aspose::Words::NumberStyle::Custom, customNumberStyleFormat));
```


يُظهر كيفية تعيين تنسيق نمط الرقم المخصص.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with leading zero.docx");

doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::ParagraphCollection> paras = doc->get_FirstSection()->get_Body()->get_Paragraphs();
ASSERT_EQ(u"001.", paras->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"0001.", paras->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"0002.", paras->idx_get(2)->get_ListLabel()->get_LabelString());

paras->idx_get(1)->get_ListFormat()->get_ListLevel()->set_CustomNumberStyleFormat(u"001, 002, 003, ...");

doc->UpdateListLabels();

ASSERT_EQ(u"001.", paras->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"001.", paras->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"002.", paras->idx_get(2)->get_ListLabel()->get_LabelString());
```

## انظر أيضًا

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
