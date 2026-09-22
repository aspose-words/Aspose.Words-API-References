---
title: "Aspose::Words::BorderCollection::get_Left yöntemi"
linktitle: "get_Left"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BorderCollection::get_Left yöntemi. C++'ta sol kenarı alır."
type: docs
weight: 9000
url: /tr/cpp/aspose.words/bordercollection/get_left/
---
## BorderCollection::get_Left method


Sol kenarı alır.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::get_Left()
```


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

## Ayrıca Bakınız

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
