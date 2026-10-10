---
title: "Aspose::Words::Font::get_TintAndShade طريقة"
linktitle: "get_TintAndShade"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Font::get_TintAndShade طريقة. يسترجع أو يعيّن قيمة مزدوجة تُفتح أو تُغيم لونًا في C++."
type: docs
weight: 54000
url: /ar/cpp/aspose.words/font/get_tintandshade/
---
## Font::get_TintAndShade method


يحصل أو يضبط قيمة مزدوجة تُفتح أو تُغمق اللون.

```cpp
double Aspose::Words::Font::get_TintAndShade()
```

## ملاحظات


القيم المسموح بها تتراوح من -1 (الأكثر قتامة) إلى 1 (الأكثر إضاءة) لهذه الخاصية.

الصفر (0) محايد.

## أمثلة



يعرض كيفية إنشاء واستخدام النمط المتعلق بالثيم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// أنشئ نمطًا ما باستخدام خصائص خط الثيم.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"ThemedStyle");
style->get_Font()->set_ThemeFont(Aspose::Words::Themes::ThemeFont::Major);
style->get_Font()->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent5);
style->get_Font()->set_TintAndShade(0.3);

builder->get_ParagraphFormat()->set_StyleName(u"ThemedStyle");
builder->Writeln(u"Text with themed style");
```

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
