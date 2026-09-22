---
title: "Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto yöntemi"
linktitle: "get_SpaceBeforeAuto"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto yöntemi. C++'ta paragraftan önceki boşluk miktarı otomatik olarak ayarlanıyorsa true döner."
type: docs
weight: 34000
url: /tr/cpp/aspose.words/paragraphformat/get_spacebeforeauto/
---
## ParagraphFormat::get_SpaceBeforeAuto method


Paragraftan önceki boşluk miktarı otomatik olarak ayarlanmışsa doğru.

```cpp
bool Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto()
```

## Açıklamalar


**true** olarak ayarlandığında, [SpaceBefore](../get_spacebefore/) etkisini geçersiz kılar.

Paragraf Space Before ve Space After'ı Auto'ya ayarladığınızda, **Microsoft** Word aşağıdaki kurallara göre paragraflar arasına otomatik olarak 14 puan boşluk ekler:

* Normally, spacing is added after all paragraphs.
* In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
* In a nested bulleted or numbered list spacing is not added.
* Spacing is normally added after a table.
* Spacing is not added after a table if it is the last block in a table cell.
* Spacing is not added after the last paragraph in a table cell.



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

## Ayrıca Bakınız

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
