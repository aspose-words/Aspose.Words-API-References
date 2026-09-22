---
title: "Aspose::Words::Drawing::Fill::get_Transparency metodu"
linktitle: "get_Transparency"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Fill::get_Transparency metodu. C++'ta belirtilen dolgunun şeffaflık derecesini 0.0 (opak) ile 1.0 (şeffaf) arasında bir değer olarak alır veya ayarlar."
type: docs
weight: 21000
url: /tr/cpp/aspose.words.drawing/fill/get_transparency/
---
## Fill::get_Transparency method


Belirtilen dolgunun şeffaflık derecesini 0.0 (opak) ile 1.0 (şeffaf) arasında bir değer olarak alır veya ayarlar.

```cpp
double Aspose::Words::Drawing::Fill::get_Transparency()
```


## Örnekler



Herhangi bir dolguyu katı dolguya geri dönüştürmenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Two color gradient.docx");

// İlk Run'un Yazı Tipi için Fill nesnesini al.
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_Font()->get_Fill();

// Yazı Tipinin Fill özelliklerini kontrol et.
std::cout << System::String::Format(u"The type of the fill is: {0}", fill->get_FillType()) << std::endl;
std::cout << "The foreground color of the fill is: " << fill->get_ForeColor() << std::endl;
std::cout << "The fill is transparent at " << (fill->get_Transparency() * 100) << "%" << std::endl;

// Dolgunun tipini tek tip yeşil renk ile Solid'a değiştir.
fill->Solid();
std::cout << "\nThe fill is changed:" << std::endl;
std::cout << System::String::Format(u"The type of the fill is: {0}", fill->get_FillType()) << std::endl;
std::cout << "The foreground color of the fill is: " << fill->get_ForeColor() << std::endl;
std::cout << "The fill transparency is " << (fill->get_Transparency() * 100) << "%" << std::endl;

doc->Save(get_ArtifactsDir() + u"Drawing.FillSolid.docx");
```

## Ayrıca Bakınız

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
