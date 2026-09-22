---
title: "Aspose::Words::TextureIndex enum"
linktitle: "TextureIndex"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TextureIndex enum. C++'da gölgelendirme dokusunu belirtir."
type: docs
weight: 125000
url: /tr/cpp/aspose.words/textureindex/
---
## TextureIndex enum


Gölgelendirme dokusunu belirtir.

```cpp
enum class TextureIndex
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Texture10Percent | 3 |  |
| Texture12Pt5Percent | 37 |  |
| Texture15Percent | 38 |  |
| Texture17Pt5Percent | 39 |  |
| Texture20Percent | 4 |  |
| Texture22Pt5Percent | 40 |  |
| Texture25Percent | 5 |  |
| Texture27Pt5Percent | 41 |  |
| Texture2Pt5Percent | 35 |  |
| Texture30Percent | 6 |  |
| Texture32Pt5Percent | 42 |  |
| Texture35Percent | 43 |  |
| Doku37Pt5Yüzde | 44 |  |
| Doku40Yüzde | 7 |  |
| Doku42Pt5Yüzde | 45 |  |
| Doku45Yüzde | 46 |  |
| Doku47Pt5Yüzde | 47 |  |
| Doku50Yüzde | 8 |  |
| Doku52Pt5Yüzde | 48 |  |
| Doku55Yüzde | 49 |  |
| Doku57Pt5Yüzde | 50 |  |
| Doku5Yüzde | 2 |  |
| Doku60Yüzde | 9 |  |
| Doku62Pt5Yüzde | 51 |  |
| Doku65Yüzde | 52 |  |
| Doku67Pt5Yüzde | 53 |  |
| Doku70Yüzde | 10 |  |
| Doku72Pt5Yüzde | 54 |  |
| Doku75Yüzde | 11 |  |
| Doku77Pt5Yüzde | 55 |  |
| Doku7Pt5Yüzde | 36 |  |
| Doku80Yüzde | 12 |  |
| Doku82Pt5Yüzde | 56 |  |
| Doku85Yüzde | 57 |  |
| Doku87Pt5Yüzde | 58 |  |
| Doku90Yüzde | 13 |  |
| Doku92Pt5Yüzde | 59 |  |
| Texture95Percent | 60 |  |
| Texture97Pt5Percent | 61 |  |
| TextureCross | 24 |  |
| TextureDarkCross | 18 |  |
| TextureDarkDiagonalCross | 19 |  |
| TextureDarkDiagonalDown | 16 |  |
| TextureDarkDiagonalUp | 17 |  |
| TextureDarkHorizontal | 14 |  |
| TextureDarkVertical | 15 |  |
| TextureDiagonalCross | 25 |  |
| TextureDiagonalDown | 22 |  |
| TextureDiagonalUp | 23 |  |
| TextureHorizontal | 20 |  |
| TextureNone | 0 |  |
| TextureSolid | 1 |  |
| TextureVertical | 21 |  |
| TextureNil | 65535 | Mevcut gölgeli bölgede hiçbir desen kullanılmayacağını belirtir (yani desen, arka plan rengiyle tamamen doldurulmalıdır). |


## Örnekler



Metni kenarlıklar ve gölgelendirme ile nasıl süsleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();
borders->set_DistanceFromText(20);
borders->idx_get(Aspose::Words::BorderType::Left)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Right)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Top)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Bottom)->set_LineStyle(Aspose::Words::LineStyle::Double);

System::SharedPtr<Aspose::Words::Shading> shading = builder->get_ParagraphFormat()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalCross);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_LightCoral());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_LightSalmon());

builder->Write(u"This paragraph is formatted with a double border and shading.");
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.ApplyBordersAndShading.docx");
```


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
