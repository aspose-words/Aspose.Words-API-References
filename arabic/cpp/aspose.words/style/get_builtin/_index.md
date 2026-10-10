---
title: "Aspose::Words::Style::get_BuiltIn طريقة"
linktitle: "get_BuiltIn"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Style::get_BuiltIn طريقة. True إذا كان هذا النمط أحد الأنماط المدمجة في MS Word في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words/style/get_builtin/
---
## Style::get_BuiltIn method


صحيح إذا كان هذا النمط أحد الأنماط المدمجة في MS Word.

```cpp
bool Aspose::Words::Style::get_BuiltIn()
```


## أمثلة



يوضح كيفية التمييز بين الأنماط المخصصة والأنماط المدمجة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// عند إنشاء مستند باستخدام Microsoft Word، أو برمجياً باستخدام Aspose.Words،
// سيأتي المستند مع مجموعة من الأنماط لتطبيقها على نصه لتعديل مظهره.
// يمكننا الوصول إلى هذه الأنماط المدمجة عبر مجموعة "Styles" في المستند.
// ستكون جميع هذه الأنماط لديها العلم "BuiltIn" مضبوط على "true".
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->idx_get(u"Emphasis");

ASSERT_TRUE(style->get_BuiltIn());

// أنشئ نمطًا مخصصًا وأضفه إلى المجموعة.
// الأنماط المخصصة مثل هذا سيكون لديها العلم "BuiltIn" مضبوط على "false".
style = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyStyle");
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
style->get_Font()->set_Name(u"Courier New");

ASSERT_FALSE(style->get_BuiltIn());
```

## انظر أيضًا

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
