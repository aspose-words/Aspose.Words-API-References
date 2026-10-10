---
title: "Aspose::Words::TextureIndex enumeración"
linktitle: "TextureIndex"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::TextureIndex enumeración. Especifica la textura de sombreado en C++."
type: docs
weight: 125000
url: /es/cpp/aspose.words/textureindex/
---
## TextureIndex enum


Especifica la textura de sombreado.

```cpp
enum class TextureIndex
```

### Valores

| Nombre | Valor | Descripción |
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
| Textura37Pt5Porcentaje | 44 |  |
| Textura40Porcentaje | 7 |  |
| Textura42Pt5Porcentaje | 45 |  |
| Textura45Porcentaje | 46 |  |
| Textura47Pt5Porcentaje | 47 |  |
| Textura50Porcentaje | 8 |  |
| Textura52Pt5Porcentaje | 48 |  |
| Textura55Porcentaje | 49 |  |
| Textura57Pt5Porcentaje | 50 |  |
| Textura5Porcentaje | 2 |  |
| Textura60Porcentaje | 9 |  |
| Textura62Pt5Porcentaje | 51 |  |
| Textura65Porcentaje | 52 |  |
| Textura67Pt5Porcentaje | 53 |  |
| Textura70Porcentaje | 10 |  |
| Textura72Pt5Porcentaje | 54 |  |
| Textura75Porcentaje | 11 |  |
| Textura77Pt5Porcentaje | 55 |  |
| Textura7Pt5Porcentaje | 36 |  |
| Textura80Porcentaje | 12 |  |
| Textura82Pt5Porcentaje | 56 |  |
| Textura85Porcentaje | 57 |  |
| Textura87Pt5Porcentaje | 58 |  |
| Textura90Porcentaje | 13 |  |
| Textura92Pt5Porcentaje | 59 |  |
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
| TextureNil | 65535 | Especifica que no se debe usar ningún patrón en la región sombreada actual (es decir, el patrón debe ser un relleno completo con el color de fondo). |


## Ejemplos



Muestra cómo decorar el texto con bordes y sombreado.
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


Muestra cómo aplicar un borde de contorno a una tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Alinea la tabla al centro de la página.
table->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);

// Elimina cualquier borde y sombreado existente de la tabla.
table->ClearBorders();
table->ClearShading();

// Añade bordes verdes al contorno de la tabla.
table->SetBorder(Aspose::Words::BorderType::Left, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Right, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Bottom, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);

// Rellena las celdas con un color sólido verde claro.
table->SetShading(Aspose::Words::TextureIndex::TextureSolid, System::Drawing::Color::get_LightGreen(), System::Drawing::Color::Empty);

doc->Save(get_ArtifactsDir() + u"Table.SetOutlineBorders.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
