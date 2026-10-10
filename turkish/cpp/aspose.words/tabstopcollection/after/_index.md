---
title: "Aspose::Words::TabStopCollection::After yöntemi"
linktitle: "Sonra"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TabStopCollection::After yöntemi. C++'ta belirtilen konumun sağındaki ilk sekme durağını alır."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/tabstopcollection/after/
---
## TabStopCollection::After method


Belirtilen konumun sağındaki ilk sekme durak noktasını alır.

```cpp
System::SharedPtr<Aspose::Words::TabStop> Aspose::Words::TabStopCollection::After(double position)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| konum | double | Referans konumu (nokta cinsinden). |

### ReturnValue

Uygun bir sekme durak bulunamazsa **null** olan bir sekme durak nesnesi.
## Açıklamalar


Sekme duraklarını [Alignment](../../tabstop/get_alignment/) [Bar](../../tabalignment/) ayarlanmış olanları atlar.

## Örnekler



Bir belgenin sekme durak noktası koleksiyonuyla nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = builder->get_ParagraphFormat()->get_TabStops();

// 72 puan, Microsoft Word sekme durak cetvelinde bir "inç"tir.
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(72.0));
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(432.0, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Dashes));

ASSERT_EQ(2, tabStops->get_Count());
ASSERT_FALSE(tabStops->idx_get(0)->get_IsClear());
ASSERT_FALSE(System::ObjectExt::Equals(tabStops->idx_get(0), tabStops->idx_get(1)));

// Her "tab" karakteri, oluşturucunun imlecini bir sonraki sekme durak noktasının konumuna götürür.
builder->Writeln(u"Start\tTab 1\tTab 2");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(2, paragraphs->get_Count());

// Her paragraf, değerlerini belge oluşturucusunun sekme durak noktası koleksiyonundan kopyalayan kendi sekme durak noktası koleksiyonunu alır.
ASPOSE_ASSERT_EQ(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());
ASPOSE_ASSERT_NS(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());

// Bir sekme durak noktası koleksiyonu, belirli konumlardan önce ve sonra bulunan TabStop'lara işaret edebilir.
ASPOSE_ASSERT_EQ(72.0, tabStops->Before(100.0)->get_Position());
ASPOSE_ASSERT_EQ(432.0, tabStops->After(100.0)->get_Position());

// Varsayılan sekme davranışına geri dönmek için bir paragrafın sekme durak noktası koleksiyonunu temizleyebiliriz.
paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->Clear();

ASSERT_EQ(0, paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->get_Count());

doc->Save(get_ArtifactsDir() + u"TabStopCollection.TabStopCollection.docx");
```

## Ayrıca Bakınız

* Class [TabStop](../../tabstop/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
