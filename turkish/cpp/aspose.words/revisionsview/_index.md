---
title: "Aspose::Words::RevisionsView enum"
linktitle: "RevisionsView"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::RevisionsView enum. Bir belgenin orijinal ya da revize edilmiş sürümüyle çalışılıp çalışılmayacağını C++'ta belirtmeye olanak tanır."
type: docs
weight: 112000
url: /tr/cpp/aspose.words/revisionsview/
---
## RevisionsView enum


Bir belgeyle orijinal mi yoksa revize edilmiş sürümle mi çalışılacağını belirtmeye olanak tanır.

```cpp
enum class RevisionsView
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Orijinal | 0 | Belgenin orijinal sürümünü belirtir. |
| Final | 1 | Belgenin revize edilmiş sürümünü belirtir. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
