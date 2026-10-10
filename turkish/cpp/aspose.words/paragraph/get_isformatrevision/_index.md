---
title: "Aspose::Words::Paragraph::get_IsFormatRevision yöntemi"
linktitle: "get_IsFormatRevision"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Paragraph::get_IsFormatRevision yöntemi. Nesnenin biçimlendirmesi Microsoft Word'de değişiklik izleme etkinken değiştirildiyse true döndürür C++ içinde."
type: docs
weight: 12000
url: /tr/cpp/aspose.words/paragraph/get_isformatrevision/
---
## Paragraph::get_IsFormatRevision method


Değişiklik izleme etkinleştirildiği sırada Microsoft Word'de nesnenin biçimlendirmesi değiştirildiyse true döndürür.

```cpp
bool Aspose::Words::Paragraph::get_IsFormatRevision()
```


## Örnekler



Bir paragrafın biçim revizyonu olup olmadığını nasıl kontrol edeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Format revision.docx");

// Bu paragraf bir "Format" revizyonudur; bu, mevcut metnin biçimlendirmesini değiştirdiğimizde oluşur.
// Microsoft Word'de "Review" -> "Track changes" yoluyla revizyonları izlerken.
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_IsFormatRevision());
```

## Ayrıca Bakınız

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
