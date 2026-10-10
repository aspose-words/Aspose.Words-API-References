---
title: "Aspose::Words::TabLeader enum"
linktitle: "TabLeader"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TabLeader enum. C++'da sekme karakterinin altında gösterilen lider çizgi tipini belirtir."
type: docs
weight: 121000
url: /tr/cpp/aspose.words/tableader/
---
## TabLeader enum


Sekme karakterinin altında gösterilen lider çizgi tipini belirtir.

```cpp
enum class TabLeader
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 | Lider çizgi gösterilmez. |
| Noktalar | 1 | Lider çizgi noktalardan oluşur. |
| Çizgiler | 2 | Lider çizgi çizgilerden oluşur. |
| Çizgi | 3 | Lider çizgi tek bir çizgidir. |
| Kalın | 4 | Lider çizgi tek bir kalın çizgidir. |
| MiddleDot | 5 | Lider çizgi orta noktalardan oluşur. |


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
