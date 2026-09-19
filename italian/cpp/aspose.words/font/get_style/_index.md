---
title: "Metodo Aspose::Words::Font::get_Style"
linktitle: "get_Style"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_Style. Ottiene o imposta lo stile di carattere applicato a questa formattazione in C++."
type: docs
weight: 42000
url: /it/cpp/aspose.words/font/get_style/
---
## Font::get_Style method


Ottiene o imposta lo stile del carattere applicato a questa formattazione.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::Font::get_Style()
```


## Esempi



Applica una doppia sottolineatura a tutti i run in un documento che sono formattati con stili di carattere personalizzati.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci uno stile personalizzato e applicalo al testo creato utilizzando un document builder.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyStyle");
style->get_Font()->set_Color(System::Drawing::Color::get_Red());
style->get_Font()->set_Name(u"Courier New");

builder->get_Font()->set_StyleName(u"MyStyle");
builder->Write(u"This text is in a custom style.");

// Itera su ogni run e aggiungi una doppia sottolineatura a ogni stile personalizzato.
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

## Vedi anche

* Class [Style](../../style/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
