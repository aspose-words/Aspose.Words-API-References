---
title: "Метод Aspose::Words::Font::get_Style"
linktitle: "get_Style"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_Style. Получает или задает стиль символов, применяемый к этому форматированию, в C++."
type: docs
weight: 42000
url: /ru/cpp/aspose.words/font/get_style/
---
## Font::get_Style method


Получает или задает стиль символов, применяемый к этому форматированию.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::Font::get_Style()
```


## Примеры



Применяет двойное подчеркивание ко всем фрагментам в документе, отформатированным с помощью пользовательских стилей символов.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте пользовательский стиль и примените его к тексту, созданному с помощью Document Builder.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyStyle");
style->get_Font()->set_Color(System::Drawing::Color::get_Red());
style->get_Font()->set_Name(u"Courier New");

builder->get_Font()->set_StyleName(u"MyStyle");
builder->Write(u"This text is in a custom style.");

// Итерируйте каждый фрагмент и добавьте двойное подчеркивание к каждому пользовательскому стилю.
for (auto&& run : System::IterateOver<Aspose::Words::Run>(doc->GetChildNodes(Aspose::Words::NodeType::Run, true)))
{
    System::SharedPtr<Aspose::Words::Style> charStyle = run->get_Font()->get_Style();

    if (!charStyle->get_BuiltIn())
    {
        run->get_Font()->set_Underline(Aspose::Words::Underline::Double);
    }
}

doc->Save(get_ArtifactsDir() + u"Font.Style.docx");
```

## См. также

* Class [Style](../../style/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
