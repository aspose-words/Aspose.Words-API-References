---
title: "Aspose::Words::TextureIndex enum"
linktitle: "TextureIndex"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TextureIndex enum. Specifica la trama di ombreggiatura in C++."
type: docs
weight: 125000
url: /it/cpp/aspose.words/textureindex/
---
## TextureIndex enum


Specifica la trama dell'ombreggiatura.

```cpp
enum class TextureIndex
```

### Valori

| Nome | Valore | Descrizione |
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
| Trama37Pt5Percento | 44 |  |
| Trama40Percento | 7 |  |
| Trama42Pt5Percento | 45 |  |
| Trama45Percento | 46 |  |
| Trama47Pt5Percento | 47 |  |
| Trama50Percento | 8 |  |
| Trama52Pt5Percento | 48 |  |
| Trama55Percento | 49 |  |
| Trama57Pt5Percento | 50 |  |
| Trama5Percento | 2 |  |
| Trama60Percento | 9 |  |
| Trama62Pt5Percento | 51 |  |
| Trama65Percento | 52 |  |
| Trama67Pt5Percento | 53 |  |
| Trama70Percento | 10 |  |
| Trama72Pt5Percento | 54 |  |
| Trama75Percento | 11 |  |
| Trama77Pt5Percento | 55 |  |
| Trama7Pt5Percento | 36 |  |
| Trama80Percento | 12 |  |
| Trama82Pt5Percento | 56 |  |
| Trama85Percento | 57 |  |
| Trama87Pt5Percento | 58 |  |
| Trama90Percento | 13 |  |
| Trama92Pt5Percento | 59 |  |
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
| TextureNil | 65535 | Specifica che non deve essere utilizzato alcun motivo nella regione ombreggiata corrente (cioè il motivo deve essere un riempimento completo con il colore di sfondo). |


## Esempi



Mostra come decorare il testo con bordi e ombreggiatura.
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


Mostra come applicare un bordo di contorno a una tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Allinea la tabella al centro della pagina.
table->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);

// Rimuovi eventuali bordi e ombreggiature esistenti dalla tabella.
table->ClearBorders();
table->ClearShading();

// Aggiungi bordi verdi al contorno della tabella.
table->SetBorder(Aspose::Words::BorderType::Left, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Right, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Bottom, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);

// Riempi le celle con un colore verde chiaro solido.
table->SetShading(Aspose::Words::TextureIndex::TextureSolid, System::Drawing::Color::get_LightGreen(), System::Drawing::Color::Empty);

doc->Save(get_ArtifactsDir() + u"Table.SetOutlineBorders.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
