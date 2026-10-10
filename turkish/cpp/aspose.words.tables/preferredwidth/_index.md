---
title: "Aspose::Words::Tables::PreferredWidth class"
linktitle: "PreferredWidth"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::PreferredWidth class. Bir tablo veya hücrenin tercih edilen genişliğini belirtmek için kullanılan bir değeri ve ölçü birimini temsil eder. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.tables/preferredwidth/
---
## PreferredWidth class


Bir tablo veya hücrenin tercih edilen genişliğini belirtmek için kullanılan bir değeri ve ölçü birimini temsil eder. Daha fazla bilgi edinmek için [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) dokümantasyon makalesini ziyaret edin.

```cpp
class PreferredWidth : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| static [Auto](./auto/)() | "Tercih edilen genişlik belirtilmemiş" değerini temsil eden bir örnek döndürür. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | Belirtilen [PreferredWidth](./) değerinin mevcut [PreferredWidth](./) ile eşit olup olmadığını belirler. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Belirtilen nesnenin mevcut nesneyle değer olarak eşit olup olmadığını belirler. |
| static [FromPercent](./frompercent/)(double) | Yüzde olarak belirtilen bir tercih edilen genişliği temsil eden yeni bir örnek döndüren bir oluşturma yöntemi. |
| static [FromPoints](./frompoints/)(double) | Puan sayısı kullanılarak belirtilen bir tercih edilen genişliği temsil eden yeni bir örnek döndüren bir oluşturma yöntemi. |
| [get_Type](./get_type/)() const | Bu tercih edilen genişlik değeri için kullanılan ölçü birimini alır. |
| [get_Value](./get_value/)() const | Tercih edilen genişlik değerini alır. Ölçü birimi [Type](./get_type/) özelliğinde belirtilir. |
| [GetHashCode](./gethashcode/)() const override | Bu tip için bir karma (hash) işlevi olarak hizmet verir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | Bu nesnenin değerini gösteren kullanıcı dostu bir dize döndürür. |
| static [Type](./type/)() |  |
## Açıklamalar


Tercih edilen genişlik yüzde, nokta sayısı veya özel bir "none/auto" değeri olarak belirtilebilir.

Bu sınıfın örnekleri değiştirilemez.

## Örnekler



Bir tablonun sayfanın genişliğinin %50'sine otomatik olarak sığdırılmasını nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell #1");
builder->InsertCell();
builder->Write(u"Cell #2");
builder->InsertCell();
builder->Write(u"Cell #3");

table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(50));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithPreferredWidth.docx");
```


Tablo hücreleri için tercih edilen bir genişliğin nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// "PreferredWidth" sınıfını tablo hücrelerine uygulamanın iki yolu vardır.
// 1 -  Noktalara dayalı mutlak bir tercih edilen genişlik ayarlayın:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(40));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightYellow());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

// 2 -  Tablo genişliğinin yüzdesine dayalı göreceli bir tercih edilen genişlik ayarlayın:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(20));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

builder->InsertCell();

// Tercih edilen genişlik belirtilmemiş bir hücre, mevcut alanın geri kalanını kaplayacaktır.
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());

// "PreferredWidth" özelliğinin her yapılandırması yeni bir nesne oluşturur.
ASSERT_NE(System::ObjectExt::GetHashCode(table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_PreferredWidth()), System::ObjectExt::GetHashCode(builder->get_CellFormat()->get_PreferredWidth()));

builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightGreen());
builder->Writeln(u"Automatically sized cell.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
