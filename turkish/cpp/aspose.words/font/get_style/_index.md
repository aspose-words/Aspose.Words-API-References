---
title: "Aspose::Words::Font::get_Style yöntemi"
linktitle: "get_Style"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_Style yöntemi. C++'ta bu biçimlendirmeye uygulanan karakter stilini alır veya ayarlar."
type: docs
weight: 42000
url: /tr/cpp/aspose.words/font/get_style/
---
## Font::get_Style method


Bu biçimlendirmeye uygulanan karakter stilini alır veya ayarlar.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::Font::get_Style()
```


## Örnekler



Özel karakter stilleriyle biçimlendirilmiş bir belgedeki tüm koşullara çift alt çizgi uygular.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Özel bir stil ekleyin ve belge oluşturucu kullanarak oluşturulan metne uygulayın.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyStyle");
style->get_Font()->set_Color(System::Drawing::Color::get_Red());
style->get_Font()->set_Name(u"Courier New");

builder->get_Font()->set_StyleName(u"MyStyle");
builder->Write(u"This text is in a custom style.");

// Her koşulu yineleyin ve her özel stile çift alt çizgi ekleyin.
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

## Ayrıca Bakınız

* Class [Style](../../style/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
