---
title: "Aspose::Words::TabAlignment enum"
linktitle: "TabAlignment"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TabAlignment enum. C++'da bir sekme durağının hizalamasını/türünü belirtir."
type: docs
weight: 120000
url: /tr/cpp/aspose.words/tabalignment/
---
## TabAlignment enum


Bir sekme durağının hizalamasını/türünü belirtir.

```cpp
enum class TabAlignment
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Sol | 0 | Sekme durağından sonraki metni sola hizalar. |
| Orta | 1 | Metni sekme durağının etrafında ortalar. |
| Sağ | 2 | Sekme durağında metni sağa hizalar. |
| Decimal | 3 | Metni ondalık noktada hizalar. |
| Bar | 4 | Sekme durağı konumunda dikey bir çubuk çizer. |
| List | 6 | Sekme, bir liste öğesindeki sayı/işaret ve metin arasında bir ayırıcıdır. |
| Clear | 7 | Bu konumdaki tüm sekme duraklarını temizler. |


## Örnekler



Bir paragraf için özel sekme duraklarının nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Bu koleksiyonda sekme durakları olmayan bir paragrafta isek,
// İmleç, Microsoft Word'de Tab tuşuna her bastığımızda 36 puan atlayacaktır.
ASSERT_EQ(0, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetEffectiveTabStops()->get_Length());

// Microsoft Word'de, "View" sekmesi aracılığıyla cetveli etkinleştirirsek özel sekme durakları ekleyebiliriz.
// Bu cetveldeki her bir birim iki varsayılan sekme durağına eşittir, yani 72 puan.
// Özel sekme duraklarını programlı olarak şöyle ekleyebiliriz.
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_TabStops();
tabStops->Add(72, Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dots);
tabStops->Add(216, Aspose::Words::TabAlignment::Center, Aspose::Words::TabLeader::Dashes);
tabStops->Add(360, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Line);

// Microsoft Word'de bu sekme duraklarını "View" -> "Show" -> "Ruler" yoluyla cetveli etkinleştirerek görebiliriz.
ASSERT_EQ(3, para->GetEffectiveTabStops()->get_Length());

// Eklediğimiz herhangi bir sekme karakteri, cetveldeki sekme duraklarını kullanacak ve olabilir,
// sekme liderinin değerine bağlı olarak, sekme başlangıcı ile varış noktası arasında bir çizgi bırakabilir.
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"\tTab 1\tTab 2\tTab 3"));

doc->Save(get_ArtifactsDir() + u"Paragraph.TabStops.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
