---
title: "Aspose::Words::Settings::OdsoFieldMapData class"
linktitle: "OdsoFieldMapData"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::OdsoFieldMapData sınıfı. Belirli bir sütunun dış veri kaynağında nasıl belge içindeki önceden tanımlanmış birleştirme alanlarına eşleneceğini belirtir. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class


Harici veri kaynağındaki bir sütunun belgede önceden tanımlanmış birleştirme alanlarına nasıl eşleneceğini belirtir. Daha fazla bilgi için, [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) dokümantasyon makalesini ziyaret edin.

```cpp
class OdsoFieldMapData : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Clone](./clone/)() | Bu nesnenin derin bir kopyasını döndürür. |
| [get_Column](./get_column/)() const | Dış veri kaynağındaki sütunun sıfır tabanlı indeksini, belirli bir MERGEFIELD alanının yerel adıyla eşlenecek şekilde belirtir. Varsayılan değer 0'dır. |
| [get_MappedName](./get_mappedname/)() const | Bu alan eşlemesindeki [Column](./get_column/) özelliğiyle belirtilen sütun numarasına eşlenecek önceden tanımlanmış birleştirme alanı adını belirtir. Varsayılan değer boş bir dizedir. |
| [get_Name](./get_name/)() const | Dış veri kaynağındaki, [Column](./get_column/) özelliğiyle belirtilen indeksli sütun için sütun adını belirtir. Varsayılan değer boş bir dizedir. |
| [get_Type](./get_type/)() const | Belirli bir posta birleştirme alanının verilen dış veri kaynağındaki bir sütuna eşlenip eşlenmediğini belirtir. Varsayılan değer [Default](../odsofieldmappingtype/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OdsoFieldMapData](./odsofieldmapdata/)() |  |
| [set_Column](./set_column/)(int32_t) | Dış veri kaynağındaki sütunun sıfır tabanlı indeksini, belirli bir MERGEFIELD alanının yerel adıyla eşlenecek şekilde belirtir. Varsayılan değer 0'dır. |
| [set_MappedName](./set_mappedname/)(const System::String\&) | Bu alan eşlemesindeki [Column](./get_column/) özelliğiyle belirtilen sütun numarasına eşlenecek önceden tanımlanmış birleştirme alanı adını belirtir. Varsayılan değer boş bir dizedir. |
| [set_Name](./set_name/)(const System::String\&) | Dış veri kaynağındaki, [Column](./get_column/) özelliğiyle belirtilen indeksli sütun için sütun adını belirtir. Varsayılan değer boş bir dizedir. |
| [set_Type](./set_type/)(Aspose::Words::Settings::OdsoFieldMappingType) | Belirli bir posta birleştirme alanının verilen dış veri kaynağındaki bir sütuna eşlenip eşlenmediğini belirtir. Varsayılan değer [Default](../odsofieldmappingtype/). |
| static [Type](./type/)() |  |
## Açıklamalar


Microsoft Word, bir belgeye MERGEFIELD olarak eklenebilen veya ADDRESSBLOCK ya da GREETINGLINE alanlarında kullanılabilen bazı önceden tanımlanmış birleştirme alanı adları sağlar. [OdsoFieldMapData](./) içinde belirtilen bilgiler, dış veri kaynağındaki bir sütunu tek bir önceden tanımlanmış birleştirme alanına eşlemeye olanak tanır.

## Ayrıca Bakınız

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
