---
title: "Aspose::Words::ConditionalStyle::ClearFormatting yöntemi"
linktitle: "ClearFormatting"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ConditionalStyle::ClearFormatting yöntemi. C++'da bu koşullu stilin biçimlendirmesini temizler."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/conditionalstyle/clearformatting/
---
## ConditionalStyle::ClearFormatting method


Bu koşullu stilin biçimlendirmesini temizler.

```cpp
void Aspose::Words::ConditionalStyle::ClearFormatting()
```


## Örnekler



Koşullu tablo stillerinin nasıl sıfırlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"First row");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Last row");
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
table->set_Style(tableStyle);

// Tablo stilini, tablonun ilk satırının kenarlıklarını kırmızı renkle renklendirecek şekilde ayarlayın.
tableStyle->get_ConditionalStyles()->get_FirstRow()->get_Borders()->set_Color(System::Drawing::Color::get_Red());

// Tablo stilini, tablonun son satırının kenarlıklarını mavi renkle renklendirecek şekilde ayarlayın.
tableStyle->get_ConditionalStyles()->get_LastRow()->get_Borders()->set_Color(System::Drawing::Color::get_Blue());

// Aşağıda, koşullu stilleri temizlemek için "ClearFormatting" yöntemini kullanmanın iki yolu verilmiştir.
// 1 -  Tablonun belirli bir bölümü için koşullu stilleri temizleyin:
tableStyle->get_ConditionalStyles()->idx_get(0)->ClearFormatting();

ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, tableStyle->get_ConditionalStyles()->get_FirstRow()->get_Borders()->get_Color());

// 2 -  Tüm tablo için koşullu stilleri temizleyin:
tableStyle->get_ConditionalStyles()->ClearFormatting();

ASSERT_TRUE(tableStyle->get_ConditionalStyles()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::ConditionalStyle>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::ConditionalStyle> s)>>([](System::SharedPtr<Aspose::Words::ConditionalStyle> s) -> bool
{
    return s->get_Borders()->get_Color() == System::Drawing::Color::Empty;
}))));
```

## Ayrıca Bakınız

* Class [ConditionalStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
