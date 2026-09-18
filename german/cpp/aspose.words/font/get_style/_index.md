---
title: "Aspose::Words::Font::get_Style Methode"
linktitle: "get_Style"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_Style Methode. Gibt den Zeichenstil zurück oder legt ihn fest, der auf diese Formatierung in C++ angewendet wird."
type: docs
weight: 42000
url: /de/cpp/aspose.words/font/get_style/
---
## Font::get_Style method


Liest oder legt den Zeichenstil fest, der auf diese Formatierung angewendet wird.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::Font::get_Style()
```


## Beispiele



Wendet eine doppelte Unterstreichung auf alle Laufabschnitte in einem Dokument an, die mit benutzerdefinierten Zeichenstilen formatiert sind.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie einen benutzerdefinierten Stil ein und wenden Sie ihn auf Text an, der mit einem Dokumenten-Builder erstellt wurde.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyStyle");
style->get_Font()->set_Color(System::Drawing::Color::get_Red());
style->get_Font()->set_Name(u"Courier New");

builder->get_Font()->set_StyleName(u"MyStyle");
builder->Write(u"This text is in a custom style.");

// Iterieren Sie über jeden Lauf und fügen Sie jedem benutzerdefinierten Stil eine doppelte Unterstreichung hinzu.
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

## Siehe auch

* Class [Style](../../style/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
