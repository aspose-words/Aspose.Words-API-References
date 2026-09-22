---
title: "Aspose::Words::Tables::Table::SetShading yöntemi"
linktitle: "SetShading"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Table::SetShading yöntemi. C++'da tüm tabloya belirtilen değerlerde gölgelendirme ayarlar."
type: docs
weight: 70000
url: /tr/cpp/aspose.words.tables/table/setshading/
---
## Table::SetShading method


Tüm tablo üzerinde gölgelendirmeyi belirtilen değerlere ayarlar.

```cpp
void Aspose::Words::Tables::Table::SetShading(Aspose::Words::TextureIndex texture, System::Drawing::Color foregroundColor, System::Drawing::Color backgroundColor)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doku | Aspose::Words::TextureIndex | Uygulanacak doku. |
| foregroundColor | System::Drawing::Color | Dokunun rengi. |
| backgroundColor | System::Drawing::Color | Arka plan doldurmanın rengi. |

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

* Enum [TextureIndex](../../../aspose.words/textureindex/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
