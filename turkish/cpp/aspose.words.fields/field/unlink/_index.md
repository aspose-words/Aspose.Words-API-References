---
title: "Aspose::Words::Fields::Field::Unlink yöntemi"
linktitle: "Bağlantıyı Kaldır"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::Field::Unlink yöntemi. C++'ta alanın bağlantısını kaldırır."
type: docs
weight: 22000
url: /tr/cpp/aspose.words.fields/field/unlink/
---
## Field::Unlink method


Alan bağlantısını kaldırır.

```cpp
bool Aspose::Words::Fields::Field::Unlink()
```


### ReturnValue

**true** if the field has been unlinked, otherwise **false**.
## Açıklamalar


Alanı en son sonucu ile değiştirir.

XE (Dizin Girişi) alanları ve SEQ (Sıra) alanları gibi bazı alanlar bağlantısı kesilemez.

## Örnekler



Bir alanın bağlantısını nasıl keseceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");
doc->get_Range()->get_Fields()->idx_get(1)->Unlink();
```

## Ayrıca Bakınız

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
