---
title: "Aspose::Words::Font::get_Style metod"
linktitle: "get_Style"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_Style metod. Hämtar eller anger teckenstilen som tillämpas på denna formatering i C++."
type: docs
weight: 42000
url: /sv/cpp/aspose.words/font/get_style/
---
## Font::get_Style method


Hämtar eller anger teckenstilen som tillämpas på denna formatering.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::Font::get_Style()
```


## Exempel



Tillämpar en dubbel understrykning på alla run i ett dokument som är formaterade med anpassade teckenstilar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en anpassad stil och tillämpa den på text som skapats med en dokumentbyggare.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyStyle");
style->get_Font()->set_Color(System::Drawing::Color::get_Red());
style->get_Font()->set_Name(u"Courier New");

builder->get_Font()->set_StyleName(u"MyStyle");
builder->Write(u"This text is in a custom style.");

// Iterera över varje run och lägg till en dubbel understrykning för varje anpassad stil.
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

## Se även

* Class [Style](../../style/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
