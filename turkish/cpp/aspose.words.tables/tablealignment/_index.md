---
title: "Aspose::Words::Tables::TableAlignment enum"
linktitle: "TableAlignment"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::TableAlignment enum. C++'ta satır içi bir tablo için hizalamayı belirtir."
type: docs
weight: 14000
url: /tr/cpp/aspose.words.tables/tablealignment/
---
## TableAlignment enum


Satır içi bir tablo için hizalamayı belirtir.

```cpp
enum class TableAlignment
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Sol | 0 | Tablo sola hizalanmıştır. |
| Orta | 1 | Tablo ortalanmıştır. |
| Sağ | 2 | Tablo sağa hizalanmıştır. |


## Örnekler



Bir tabloya dış kenarlık nasıl uygulanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Tabloyu sayfanın ortasına hizalayın.
table->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);

// Tablodaki mevcut tüm kenarlıkları ve gölgelendirmeyi temizleyin.
table->ClearBorders();
table->ClearShading();

// Tablonun dış kenarına yeşil kenarlıklar ekleyin.
table->SetBorder(Aspose::Words::BorderType::Left, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Right, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Bottom, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);

// Hücreleri açık yeşil katı bir renk ile doldurun.
table->SetShading(Aspose::Words::TextureIndex::TextureSolid, System::Drawing::Color::get_LightGreen(), System::Drawing::Color::Empty);

doc->Save(get_ArtifactsDir() + u"Table.SetOutlineBorders.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
