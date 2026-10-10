---
title: "Aspose::Words::ParagraphAlignment enum"
linktitle: "ParagraphAlignment"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphAlignment enum. C++'da bir paragrafta metin hizalamasını belirtir."
type: docs
weight: 110000
url: /tr/cpp/aspose.words/paragraphalignment/
---
## ParagraphAlignment enum


Bir paragrafta metin hizalamasını belirtir.

```cpp
enum class ParagraphAlignment
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Sol | 0 | Metin sola hizalanır. |
| Orta | 1 | Metin yatay olarak ortalanır. |
| Sağ | 2 | Metin sağa hizalanır. |
| İki yana yasla | 3 | Metin hem sola hem sağa hizalanır. |
| Distributed | 4 | Metin eşit olarak dağıtılır. |
| ArabicMediumKashida | 5 | Yalnızca Arapça. Metin için Kashida uzunluğu, tüketici tarafından belirlenen orta bir uzunluğa uzatılır. |
| ArabicHighKashida | 7 | Yalnızca Arapça. Metin için Kashida uzunluğu mümkün olan en geniş uzunluğa uzatılır. |
| ArabicLowKashida | 8 | Yalnızca Arapça. Metin için Kashida uzunluğu biraz daha uzun bir uzunluğa uzatılır. |
| ThaiDistributed | 9 | Yalnızca Tayca. Metin Tayca için bir optimizasyonla iki yana yaslanır. |
| MathElementCenterAsGroup | 10 | Satırdaki tek [Math](../../aspose.words.math/) öğe, 'Centered As Group' olarak hizalanmıştır. |


## Örnekler



Aspose.Words belgesini elle nasıl oluşturacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Boş bir belge bir bölüm, bir gövde ve bir paragraf içerir.
// "RemoveAllChildren" yöntemini çağırarak bu düğümlerin tümünü kaldırın,
// ve hiçbir çocuğu olmayan bir belge düğümü elde edin.
doc->RemoveAllChildren();

// Bu belge artık içerik ekleyebileceğimiz birleşik alt düğümlere sahip değil.
// Eğer düzenlemek istersek, düğüm koleksiyonunu yeniden doldurmamız gerekecek.
// İlk olarak yeni bir bölüm oluşturun ve ardından kök belge düğümüne çocuk olarak ekleyin.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Bölüm için bazı sayfa ayarı özelliklerini ayarlayın.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Bir bölüm bir gövdeye ihtiyaç duyar, bu gövde tüm içeriğini barındırır ve gösterir
// sayfada bölümün başlığı ile altbilgisi arasındaki alanda.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Bir paragraf oluşturun, bazı biçimlendirme özelliklerini ayarlayın ve ardından onu gövdenin bir çocuğu olarak ekleyin.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Son olarak, belgeye içerik ekleyin. Bir run oluşturun,
// Görünümünü ve içeriğini ayarlayın, ardından onu paragrafın bir çocuğu olarak ekleyin.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
