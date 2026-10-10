---
title: "طريقة Aspose::Words::Lists::ListLevel::GetEffectiveValue"
linktitle: "GetEffectiveValue"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Lists::ListLevel::GetEffectiveValue. تُبلغ عن تمثيل السلسلة لكائن ListLevel للفهرس المحدد لعنصر القائمة. تُحدد المعلمات نمط الرقم وسلسلة تنسيق اختيارية تُستخدم عندما يتم تحديد \"Custom\" في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel::GetEffectiveValue method


يُبلغ عن تمثيل السلسلة لكائن [ListLevel](../) للفهارس المحددة لعنصر القائمة. تُحدد المعلمات الـ[NumberStyle](../../../aspose.words/numberstyle/) وسلسلة تنسيق اختيارية تُستخدم عندما يتم تحديد [Custom](../../../aspose.words/numberstyle/).

```cpp
static System::String Aspose::Words::Lists::ListLevel::GetEffectiveValue(int32_t index, Aspose::Words::NumberStyle numberStyle, const System::String &customNumberStyleFormat)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| index | int32_t | فهرس عنصر القائمة (يجب أن يكون ضمن النطاق من 1 إلى 32767). |
| numberStyle | Aspose::Words::NumberStyle | الـ[NumberStyle](../../../aspose.words/numberstyle/) لكائن [ListLevel](../). |
| customNumberStyleFormat | const System::String\& | سلسلة التنسيق الاختيارية المستخدمة عندما يتم تحديد [Custom](../../../aspose.words/numberstyle/) (مثال: "a, ç, ĝ, ..."). في الحالات الأخرى، يجب أن تكون هذه المعلمة **null** أو فارغة. |

### ReturnValue

تمثيل السلسلة لكائن [ListLevel](../) ، الموصوف بمعامل *numberStyle* ومعامل *customNumberStyleFormat* ، في عنصر القائمة في الموضع المحدد بواسطة معامل *index*.

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

## انظر أيضًا

* Enum [NumberStyle](../../../aspose.words/numberstyle/)
* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
