---
title: "Aspose::Words::TabStop::get_IsClear yöntemi"
linktitle: "get_IsClear"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TabStop::get_IsClear yöntemi. C++'ta bu sekme noktasının bu konumdaki mevcut sekme noktalarını temizleyip temizlemediğini belirten doğru (true) değerini döndürür."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/tabstop/get_isclear/
---
## TabStop::get_IsClear method


Bu sekme durağı bu konumdaki mevcut sekme duraklarını temizlerse **true** döndürür.

```cpp
bool Aspose::Words::TabStop::get_IsClear()
```


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

* Class [TabStop](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
