---
title: "Aspose::Words::Fields::ToaCategories::idx_set metodu"
linktitle: "idx_set"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::ToaCategories::idx_set metodu. C++'ta kategori numarasına göre kategori başlığını alır veya ayarlar."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.fields/toacategories/idx_set/
---
## ToaCategories::idx_set method


Kategori numarasına göre kategori başlığını alır veya ayarlar.

```cpp
void Aspose::Words::Fields::ToaCategories::idx_set(int32_t number, const System::String &value)
```


## Örnekler



TOA alanları için bir kategori kümesi nasıl belirtileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// TOA alanları, bu koleksiyonda tanımlanan kategorilere göre girişlerini filtreleyebilir.
auto toaCategories = System::MakeObject<Aspose::Words::Fields::ToaCategories>();
doc->get_FieldOptions()->set_ToaCategories(toaCategories);

// Bu kategori koleksiyonu varsayılan değerlerle gelir; bu değerleri özel değerlerle üzerine yazabiliriz.
ASSERT_EQ(u"Cases", toaCategories->idx_get(1));
ASSERT_EQ(u"Statutes", toaCategories->idx_get(2));

toaCategories->idx_set(1, u"My Category 1");
toaCategories->idx_set(2, u"My Category 2");

// Varsayılan değerlere her zaman bu koleksiyon aracılığıyla erişebiliriz.
ASSERT_EQ(u"Cases", Aspose::Words::Fields::ToaCategories::get_DefaultCategories()->idx_get(1));
ASSERT_EQ(u"Statutes", Aspose::Words::Fields::ToaCategories::get_DefaultCategories()->idx_get(2));

// 2 TOA alanı ekleyin. TOA alanları, belgede her TA alanı için bir giriş oluşturur.
// "\c" anahtarını, koleksiyonumuzdan bir kategori indeksini seçmek için kullanın.
//  Bu anahtar ile, bir TOA alanı yalnızca şu TA alanlarından girişleri alır:
// aynı zamanda eşleşen bir kategori indeksine sahip "\c" anahtarına da sahiptir. Her TOA alanı ayrıca görüntüler
// "\c" anahtarının işaret ettiği kategori adını.
builder->InsertField(u"TOA \\c 1 \\h", nullptr);
builder->InsertField(u"TOA \\c 2 \\h", nullptr);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 2 kategori boyunca TOA girişleri ekleyin. İlk TOA alanımız bir giriş alacak,
// "\c" anahtarı da ilk kategoriye işaret eden ikinci TA alanından.
// İkinci TOA alanı, diğer iki TA alanından iki giriş alacak.
builder->InsertField(u"TA \\c 2 \\l \"entry 1\"");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertField(u"TA \\c 1 \\l \"entry 2\"");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertField(u"TA \\c 2 \\l \"entry 3\"");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.TOA.Categories.docx");
```

## Ayrıca Bakınız

* Class [ToaCategories](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
