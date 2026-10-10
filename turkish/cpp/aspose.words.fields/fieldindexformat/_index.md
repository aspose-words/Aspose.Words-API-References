---
title: "Aspose::Words::Fields::FieldIndexFormat enum"
linktitle: "FieldIndexFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldIndexFormat enum. Bir belgede FieldIndex alanları için biçimlendirmeyi C++'da belirtir."
type: docs
weight: 129000
url: /tr/cpp/aspose.words.fields/fieldindexformat/
---
## FieldIndexFormat enum


Bir belgede [FieldIndex](../fieldindex/) alanları için biçimlendirmeyi belirtir.

```cpp
enum class FieldIndexFormat
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Şablon | 0 | Şablondan. |
| Klasik | 1 | Klasik. |
| Şık | 2 | Şık. |
| Modern | 3 | Modern. |
| Madde İşaretli | 4 | Madde İşaretli. |
| Resmi | 5 | Resmi. |
| Basit | 6 | Basit. |


## Örnekler



[FieldIndex](../fieldindex/) alanlarını nasıl biçimlendireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"A");
builder->InsertBreak(Aspose::Words::BreakType::LineBreak);
builder->InsertField(u"XE \"A\"");
builder->Write(u"B");

builder->InsertField(u" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", nullptr);

doc->get_FieldOptions()->set_FieldIndexFormat(Aspose::Words::Fields::FieldIndexFormat::Fancy);
doc->UpdateFields();

doc->Save(get_ArtifactsDir() + u"Field.SetFieldIndexFormat.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
