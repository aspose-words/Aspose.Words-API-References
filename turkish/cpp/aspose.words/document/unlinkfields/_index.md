---
title: "Aspose::Words::Document::UnlinkFields metodu"
linktitle: "UnlinkFields"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::UnlinkFields metodu. C++'ta belgedeki tüm alanların bağlantısını kaldırır."
type: docs
weight: 94000
url: /tr/cpp/aspose.words/document/unlinkfields/
---
## Document::UnlinkFields method


Tüm belgede alanların bağlantısını kaldırır.

```cpp
void Aspose::Words::Document::UnlinkFields()
```

## Açıklamalar


Belgedeki tüm alanları en son sonuçlarıyla değiştirir.

Belgenin belirli bir bölümündeki alanların bağlantısını kaldırmak için [UnlinkFields](../../range/unlinkfields/) metodunu kullanın.

## Örnekler



Belgedeki tüm alanların bağlantısını nasıl kaldıracağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");

doc->UnlinkFields();
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
