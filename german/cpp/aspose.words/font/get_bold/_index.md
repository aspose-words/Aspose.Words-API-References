---
title: "Aspose::Words::Font::get_Bold Methode"
linktitle: "get_Bold"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_Bold Methode. Wahr, wenn die Schrift in C++ fett formatiert ist."
type: docs
weight: 6000
url: /de/cpp/aspose.words/font/get_bold/
---
## Font::get_Bold method


Wahr, wenn die Schriftart fett formatiert ist.

```cpp
bool Aspose::Words::Font::get_Bold()
```


## Beispiele



Zeigt, wie man formatierten Text mit [DocumentBuilder](../../documentbuilder/) einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Geben Sie die Schriftformatierung an und fügen Sie dann Text hinzu.
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
