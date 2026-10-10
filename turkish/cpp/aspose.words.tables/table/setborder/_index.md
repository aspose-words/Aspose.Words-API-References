---
title: "Aspose::Words::Tables::Table::SetBorder metodu"
linktitle: "SetBorder"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Table::SetBorder metodu. Belirtilen tablo kenarlığını belirtilen çizgi stiline, genişliğe ve renge C++'ta ayarlar."
type: docs
weight: 68000
url: /tr/cpp/aspose.words.tables/table/setborder/
---
## Table::SetBorder method


Belirtilen tablo kenarlığını belirtilen çizgi stiline, genişliğe ve renge ayarlar.

```cpp
void Aspose::Words::Tables::Table::SetBorder(Aspose::Words::BorderType borderType, Aspose::Words::LineStyle lineStyle, double lineWidth, System::Drawing::Color color, bool isOverrideCellBorders)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| borderType | Aspose::Words::BorderType | Değiştirilecek tablo kenarı. |
| lineStyle | Aspose::Words::LineStyle | Uygulanacak çizgi stili. |
| lineWidth | double | Ayarlanacak çizgi genişliği (puan cinsinden). |
| color | System::Drawing::Color | Kenarlık için kullanılacak renk. |
| isOverrideCellBorders | bool | **true** olduğunda, mevcut tüm açık hücre kenarlıklarını kaldırır. |

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

* Enum [BorderType](../../../aspose.words/bordertype/)
* Enum [LineStyle](../../../aspose.words/linestyle/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
