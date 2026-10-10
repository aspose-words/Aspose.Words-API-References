---
title: "Aspose::Words::ParagraphFormat::get_SpaceBefore method"
linktitle: "get_SpaceBefore"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_SpaceBefore method. C++'ta paragrafın önündeki boşluk miktarını (nokta cinsinden) alır veya ayarlar."
type: docs
weight: 33000
url: /tr/cpp/aspose.words/paragraphformat/get_spacebefore/
---
## ParagraphFormat::get_SpaceBefore method


Paragraftan önceki boşluk miktarını (puan cinsinden) alır veya ayarlar.

```cpp
double Aspose::Words::ParagraphFormat::get_SpaceBefore()
```

## Açıklamalar


[SpaceBeforeAuto](../get_spacebeforeauto/) **true** olduğunda etkisi yoktur.

Geçerli değerler 0 ile 1584 arasında, her iki uç dahil olmak üzere.

## Örnekler



Otomatik paragraf aralığını nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bu oluşturucu tarafından oluşturulacak paragrafların önüne ve arkasına büyük miktarda boşluk uygular.
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// Bu bayrakları otomatik aralığı uygulamak için "true" olarak ayarlayın,
// yukarıda ayarladığımız özelliklerdeki aralığı etkili bir şekilde yok sayar.
// Onları "false" olarak bırakmak, özel paragraf aralığımızı uygular.
builder->get_ParagraphFormat()->set_SpaceAfterAuto(autoSpacing);
builder->get_ParagraphFormat()->set_SpaceBeforeAuto(autoSpacing);

// Üstünde ve altında boşluk olacak iki paragraf ekleyin ve belgeyi kaydedin.
builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingAuto.docx");
```


Aynı stile sahip paragraflar arasında boşluk bırakmamanın nasıl uygulanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bu oluşturucu tarafından oluşturulacak paragrafların önüne ve arkasına büyük miktarda boşluk uygular.
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// Uygulamak için "NoSpaceBetweenParagraphsOfSameStyle" bayrağını "true" olarak ayarlayın
// aynı stile sahip paragraflar arasında boşluk bırakmaz, bu da benzer paragrafları gruplayacaktır.
// "NoSpaceBetweenParagraphsOfSameStyle" bayrağını "false" olarak bırakın
// her paragraf için eşit şekilde boşluk uygulamak için.
builder->get_ParagraphFormat()->set_NoSpaceBetweenParagraphsOfSameStyle(noSpaceBetweenParagraphsOfSameStyle);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Quote"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingSameStyle.docx");
```

## Ayrıca Bakınız

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
