---
title: "Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle yöntemi"
linktitle: "get_NoSpaceBetweenParagraphsOfSameStyle"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle yöntemi. true olduğunda, SpaceBefore ve SpaceAfter aynı stilin paragrafları arasında C++'ta yoksayılır."
type: docs
weight: 25000
url: /tr/cpp/aspose.words/paragraphformat/get_nospacebetweenparagraphsofsamestyle/
---
## ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle method


**true** olduğunda, [SpaceBefore](../get_spacebefore/) ve [SpaceAfter](../get_spaceafter/) aynı stilin paragrafları arasında yoksayılır.

```cpp
bool Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle()
```

## Açıklamalar


Bu ayar yalnızca bir paragraf stiline uygulandığında etkili olur. Doğrudan bir paragrafa uygulanırsa, hiçbir etkisi yoktur.

## Örnekler



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
