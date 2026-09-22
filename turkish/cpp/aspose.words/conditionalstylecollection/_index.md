---
title: "Aspose::Words::ConditionalStyleCollection sınıfı"
linktitle: "ConditionalStyleCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ConditionalStyleCollection sınıfı. ConditionalStyle nesnelerinin bir koleksiyonunu temsil eder. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 17000
url: /tr/cpp/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class


Bir [ConditionalStyle](../conditionalstyle/) nesnesi koleksiyonunu temsil eder. Daha fazla bilgi için [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) belge makalesini ziyaret edin.

```cpp
class ConditionalStyleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::ConditionalStyle>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Tablo stilinin tüm koşullu stillerini temizler. |
| [get_BottomLeftCell](./get_bottomleftcell/)() | Alt sol hücre stilini alır. |
| [get_BottomRightCell](./get_bottomrightcell/)() | Alt sağ hücre stilini alır. |
| [get_Count](./get_count/)() const | Koleksiyondaki koşullu stil sayısını alır. |
| [get_EvenColumnBanding](./get_evencolumnbanding/)() | Çift sütun bantlama stilini alır. |
| [get_EvenRowBanding](./get_evenrowbanding/)() | Çift satır bantlama stilini alır. |
| [get_FirstColumn](./get_firstcolumn/)() | İlk sütun stilini alır. |
| [get_FirstRow](./get_firstrow/)() | İlk satır stilini alır. |
| [get_LastColumn](./get_lastcolumn/)() | Son sütun stilini alır. |
| [get_LastRow](./get_lastrow/)() | Son satır stilini alır. |
| [get_OddColumnBanding](./get_oddcolumnbanding/)() | Tek sütun bantlama stilini alır. |
| [get_OddRowBanding](./get_oddrowbanding/)() | Tek satır bantlama stilini alır. |
| [get_TopLeftCell](./get_topleftcell/)() | Üst sol hücre stilini alır. |
| [get_TopRightCell](./get_toprightcell/)() | Üst sağ hücre stilini alır. |
| [GetEnumerator](./getenumerator/)() override | Koleksiyondaki tüm koşullu stiller üzerinde yineleme yapmak için kullanılabilecek bir enumerator nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::ConditionalStyleType) | Koşullu stil türüne göre bir [ConditionalStyle](../conditionalstyle/) nesnesi alır. |
| [idx_get](./idx_get/)(int32_t) | İndexe göre bir [ConditionalStyle](../conditionalstyle/) nesnesi alır. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Örnekler



Bir tablonun belirli alan stilleriyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell 1");
builder->InsertCell();
builder->Write(u"Cell 2");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Cell 3");
builder->InsertCell();
builder->Write(u"Cell 4");
builder->EndTable();

// Özel bir tablo stili oluşturun.
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));

// Koşullu stiller, yalnızca tablonun bazı hücrelerini etkileyen biçimlendirme değişiklikleridir
// bir koşula dayanarak, örneğin hücrelerin son satırda olması.
// Aşağıda, bir tablo stilinin koşullu stillerine "ConditionalStyles" koleksiyonundan erişmenin üç yolu verilmiştir.
// 1 -  Stil türüne göre:
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::FirstRow)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AliceBlue());

// 2 -  İndexe göre:
tableStyle->get_ConditionalStyles()->idx_get(0)->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_ConditionalStyles()->idx_get(0)->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
ASSERT_EQ(Aspose::Words::ConditionalStyleType::FirstRow, tableStyle->get_ConditionalStyles()->idx_get(0)->get_Type());

// 3 -  Özellik olarak:
tableStyle->get_ConditionalStyles()->get_FirstRow()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

// Koşullu stillere dolgu ve metin biçimlendirmesi uygulayın.
tableStyle->get_ConditionalStyles()->get_LastRow()->set_BottomPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_LeftPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_RightPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_TopPadding(10);
tableStyle->get_ConditionalStyles()->get_LastColumn()->get_Font()->set_Bold(true);

// Tüm olası stil koşullarını listeleyin.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::ConditionalStyle>>> enumerator = tableStyle->get_ConditionalStyles()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::ConditionalStyle> currentStyle = enumerator->get_Current();
        if (currentStyle != nullptr)
        {
            std::cout << System::EnumGetName(currentStyle->get_Type()) << std::endl;
        }
    }
}

// Tüm koşullu stilleri içeren özel stili tabloya uygulayın.
table->set_Style(tableStyle);

// Stilimiz varsayılan olarak bazı koşullu stilleri uygular.
ASSERT_EQ(Aspose::Words::Tables::TableStyleOptions::FirstRow | Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands, table->get_StyleOptions());

// Diğer tüm stilleri "StyleOptions" özelliği aracılığıyla kendimiz etkinleştirmemiz gerekecek.
table->set_StyleOptions(table->get_StyleOptions() | Aspose::Words::Tables::TableStyleOptions::LastRow | Aspose::Words::Tables::TableStyleOptions::LastColumn);

doc->Save(get_ArtifactsDir() + u"Table.ConditionalStyles.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
