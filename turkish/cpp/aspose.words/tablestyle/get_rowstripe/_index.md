---
title: "Aspose::Words::TableStyle::get_RowStripe yöntemi"
linktitle: "get_RowStripe"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TableStyle::get_RowStripe yöntemi. Stil tek/çift satır şeritlemesi belirttiğinde, şeritlemede dahil edilecek satır sayısını alır veya ayarlar (C++)."
type: docs
weight: 13000
url: /tr/cpp/aspose.words/tablestyle/get_rowstripe/
---
## TableStyle::get_RowStripe method


Stil tek/çift satır şeritlemesi belirttiğinde şeritlemeye dahil edilecek satır sayısını alır veya ayarlar.

```cpp
int32_t Aspose::Words::TableStyle::get_RowStripe()
```


## Örnekler



Satırlar arasında değişen koşullu tablo stillerinin nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir tablonun koşullu stilini, satır/sütuna farklı bir renk uygulamak için yapılandırabiliriz,
// satır/sütunun çift mi tek mi olduğuna bağlı olarak, değişen bir renk deseni oluşturur.
// Satır/sütun şeritlendirmesine bir n sayısı da uygulayabiliriz,
// bu, rengin her n satır/sütundan sonra bir kez değiştiği anlamına gelir.
// Tek sütun ve satırların olduğu bir tablo oluşturun; sütunlar üçlü gruplar halinde şeritlenecek.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
for (int32_t i = 0; i < 15; i++)
{
    for (int32_t j = 0; j < 4; j++)
    {
        builder->InsertCell();
        builder->Writeln(System::String::Format(u"{0} column.", (j % 2 == 0 ? System::String(u"Even") : System::String(u"Odd"))));
        builder->Write(System::String::Format(u"Row banding {0}.", (i % 3 == 0 ? System::String(u"start") : System::String(u"continuation"))));
    }
    builder->EndRow();
}
builder->EndTable();

// Tablonun tüm kenarlıklarına bir çizgi stili uygulayın.
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Double);

// Her 3 satırda bir değişecek iki rengi ayarlayın.
tableStyle->set_RowStripe(3);
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::OddRowBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::EvenRowBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightCyan());

// Her çift sütuna uygulanacak bir renk belirleyin; bu, herhangi bir özel satır rengini geçersiz kılar.
tableStyle->set_ColumnStripe(1);
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::EvenColumnBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSalmon());

table->set_Style(tableStyle);

// "StyleOptions" özelliği varsayılan olarak satır şeritlendirmesini etkinleştirir.
ASSERT_EQ(Aspose::Words::Tables::TableStyleOptions::FirstRow | Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands, table->get_StyleOptions());

// "StyleOptions" özelliğini ayrıca sütun şeritlendirmesini etkinleştirmek için kullanın.
table->set_StyleOptions(table->get_StyleOptions() | Aspose::Words::Tables::TableStyleOptions::ColumnBands);

doc->Save(get_ArtifactsDir() + u"Table.AlternatingRowStyles.docx");
```

## Ayrıca Bakınız

* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
