---
title: "Aspose::Words::Document::get_RevisionsView yöntemi"
linktitle: "get_RevisionsView"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_RevisionsView yöntemi. C++'ta bir belgenin orijinal ya da revize edilmiş sürümüyle çalışılıp çalışılmayacağını belirten bir değeri alır veya ayarlar."
type: docs
weight: 47000
url: /tr/cpp/aspose.words/document/get_revisionsview/
---
## Document::get_RevisionsView method


Belgenin orijinal mi yoksa revize edilmiş sürümüyle mi çalışılacağını gösteren değeri alır veya ayarlar.

```cpp
Aspose::Words::RevisionsView Aspose::Words::Document::get_RevisionsView() const
```


## Örnekler



Bir belgenin revize ve orijinal görünümü arasında nasıl geçiş yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions at list levels.docx");
doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();
ASSERT_EQ(u"1.", paragraphs->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"a.", paragraphs->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(System::String::Empty, paragraphs->idx_get(2)->get_ListLabel()->get_LabelString());

// Tüm revizyonlar kabul edilmiş gibi belge nesnesini görüntüleyin. Şu anda liste etiketlerini destekler.
doc->set_RevisionsView(Aspose::Words::RevisionsView::Final);

ASSERT_EQ(System::String::Empty, paragraphs->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"1.", paragraphs->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"a.", paragraphs->idx_get(2)->get_ListLabel()->get_LabelString());
```

## Ayrıca Bakınız

* Enum [RevisionsView](../../revisionsview/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
