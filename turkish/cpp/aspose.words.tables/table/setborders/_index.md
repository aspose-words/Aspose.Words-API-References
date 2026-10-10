---
title: "Aspose::Words::Tables::Table::SetBorders yöntemi"
linktitle: "SetBorders"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Table::SetBorders yöntemi. C++'da tüm tablo kenarlıklarını belirtilen çizgi stiline, genişliğe ve renge ayarlar."
type: docs
weight: 69000
url: /tr/cpp/aspose.words.tables/table/setborders/
---
## Table::SetBorders method


Tüm tablo kenarlıklarını belirtilen çizgi stiline, genişliğe ve renge ayarlar.

```cpp
void Aspose::Words::Tables::Table::SetBorders(Aspose::Words::LineStyle lineStyle, double lineWidth, System::Drawing::Color color)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| lineStyle | Aspose::Words::LineStyle | Uygulanacak çizgi stili. |
| lineWidth | double | Ayarlanacak çizgi genişliği (puan cinsinden). |
| color | System::Drawing::Color | Kenarlık için kullanılacak renk. |

## Örnekler



Bir tablo oluştururken kenarlık ve gölgelendirme renginin nasıl uygulanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir tablo başlatın ve kenarlıkları için varsayılan renk/kalınlığı ayarlayın.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
table->SetBorders(Aspose::Words::LineStyle::Single, 2.0, System::Drawing::Color::get_Black());

// Farklı arka plan renklerine sahip iki hücreli bir satır oluşturun.
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSkyBlue());
builder->Writeln(u"Row 1, Cell 1.");
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());
builder->Writeln(u"Row 1, Cell 2.");
builder->EndRow();

// Arka plan renklerini devre dışı bırakmak için hücre biçimlendirmesini sıfırla
// Yapıcı tarafından oluşturulan tüm yeni hücreler için özel bir kenarlık kalınlığı ayarlayın,
// sonra ikinci bir satır oluşturun.
builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->get_Borders()->get_Left()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Right()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Top()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Bottom()->set_LineWidth(4.0);

builder->InsertCell();
builder->Writeln(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Writeln(u"Row 2, Cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.TableBordersAndShading.docx");
```


Bir tablonun tüm kenarlıklarını bir kerede biçimlendirmenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Tablodaki tüm mevcut kenarlıkları temizle.
table->ClearBorders();

// Bu tablonun tüm dış ve iç kenarlıkları için tek bir yeşil çizgi ayarla.
table->SetBorders(Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Table.SetBorders.docx");
```

## Ayrıca Bakınız

* Enum [LineStyle](../../../aspose.words/linestyle/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
