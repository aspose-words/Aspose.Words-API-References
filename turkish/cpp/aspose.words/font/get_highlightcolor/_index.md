---
title: "Aspose::Words::Font::get_HighlightColor yöntemi"
linktitle: "get_HighlightColor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_HighlightColor yöntemi. C++'da vurgulama (işaretleyici) rengini alır veya ayarlar."
type: docs
weight: 17000
url: /tr/cpp/aspose.words/font/get_highlightcolor/
---
## Font::get_HighlightColor method


Vurgulama (işaretleyici) rengini alır veya ayarlar.

```cpp
System::Drawing::Color Aspose::Words::Font::get_HighlightColor()
```


## Örnekler



Bir metin run'ını font özelliğini kullanarak nasıl biçimlendireceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
