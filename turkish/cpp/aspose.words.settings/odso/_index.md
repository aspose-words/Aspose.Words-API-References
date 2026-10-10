---
title: "Aspose::Words::Settings::Odso class"
linktitle: "Odso"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::Odso class. Bir posta birleştirme veri kaynağı için Office Data Source Object (ODSO) ayarlarını belirtir. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.settings/odso/
---
## Odso class


Posta birleştirme veri kaynağı için Office Data Source Object (ODSO) ayarlarını belirtir. Daha fazla bilgi için, [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) dokümantasyon makalesini ziyaret edin.

```cpp
class Odso : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Clone](./clone/)() | Bu nesnenin derin bir kopyasını döndürür. |
| [get_ColumnDelimiter](./get_columndelimiter/)() const | Harici veri kaynakları içinde sütunları ayırmak için kullanılan sütun ayırıcı olarak yorumlanacak karakteri belirtir. Varsayılan değer 0'dır ve bu, tanımlı bir sütun ayırıcı olmadığı anlamına gelir. |
| [get_DataSource](./get_datasource/)() const | Posta birleştirme işlemi için bir belgeye bağlanacak harici veri kaynağının konumunu belirtir. Varsayılan değer boş bir dizedir. |
| [get_DataSourceType](./get_datasourcetype/)() const | Bu posta birleştirme için ODSO bağlantı bilgilerinin bir parçası olarak bağlanacak harici veri kaynağının türünü belirtir. Varsayılan değer [Default](../odsodatasourcetype/). |
| [get_FieldMapDatas](./get_fieldmapdatas/)() const | Harici veri kaynağından gelen sütunların belgede önceden tanımlı birleştirme alanı adlarıyla nasıl eşleneceğini belirten nesneler koleksiyonunu alır. Bu nesne asla **null** değildir. |
| [get_FirstRowContainsColumnNames](./get_firstrowcontainscolumnnames/)() const | Barındıran uygulamanın, belirtilen harici veri kaynağındaki ilk veri satırını, veri kaynağındaki her sütunun adını içeren bir başlık satırı olarak ele almasını belirtir. Varsayılan değer **false**. |
| [get_RecipientDatas](./get_recipientdatas/)() const | Posta birleştirmedeki bireysel kayıtların dahil edilmesini/çıkarılmasını belirten nesneler koleksiyonunu alır. Bu nesne asla **null** değildir. |
| [get_TableName](./get_tablename/)() const | Bir kaynağın harici veri kaynağı içinde bağlanacağı belirli veri kümesini belirtir. Varsayılan değer boş bir dizedir. |
| [get_UdlConnectString](./get_udlconnectstring/)() const | Harici bir veri kaynağına bağlanmak için kullanılan Universal Data Link (UDL) bağlantı dizesini belirtir. Varsayılan değer boş bir dizedir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Odso](./odso/)() |  |
| [set_ColumnDelimiter](./set_columndelimiter/)(char16_t) | Ayarlayıcı: [Aspose::Words::Settings::Odso::get_ColumnDelimiter](./get_columndelimiter/). |
| [set_DataSource](./set_datasource/)(const System::String\&) | Posta birleştirme işlemi için bir belgeye bağlanacak harici veri kaynağının konumunu belirtir. Varsayılan değer boş bir dizedir. |
| [set_DataSourceType](./set_datasourcetype/)(Aspose::Words::Settings::OdsoDataSourceType) | Ayarlayıcı: [Aspose::Words::Settings::Odso::get_DataSourceType](./get_datasourcetype/). |
| [set_FieldMapDatas](./set_fieldmapdatas/)(const System::SharedPtr\<Aspose::Words::Settings::OdsoFieldMapDataCollection\>\&) | Belgedeki önceden tanımlanmış birleştirme alanı adlarına haritalanan dış veri kaynağının sütunlarının nasıl eşlendiğini belirten nesneler koleksiyonunu ayarlar. Bu nesne asla **null** değildir. |
| [set_FirstRowContainsColumnNames](./set_firstrowcontainscolumnnames/)(bool) | Ayarlayıcı: [Aspose::Words::Settings::Odso::get_FirstRowContainsColumnNames](./get_firstrowcontainscolumnnames/). |
| [set_RecipientDatas](./set_recipientdatas/)(const System::SharedPtr\<Aspose::Words::Settings::OdsoRecipientDataCollection\>\&) | Posta birleştirmesinde bireysel kayıtların dahil edilmesini/çıkarılmasını belirten nesneler koleksiyonunu ayarlar. Bu nesne asla **null** değildir. |
| [set_TableName](./set_tablename/)(const System::String\&) | Bir kaynağın harici veri kaynağı içinde bağlanacağı belirli veri kümesini belirtir. Varsayılan değer boş bir dizedir. |
| [set_UdlConnectString](./set_udlconnectstring/)(const System::String\&) | Harici bir veri kaynağına bağlanmak için kullanılan Universal Data Link (UDL) bağlantı dizesini belirtir. Varsayılan değer boş bir dizedir. |
| static [Type](./type/)() |  |
## Açıklamalar


ODSO, yeni Microsoft Word sürümlerinin bir posta birleştirme belgesi için belirli veri kaynağı türlerini belirtirken tercih ettiği "yeni" yol gibi görünüyor. ODSO muhtemelen ilk olarak Microsoft Word 2000'de ortaya çıktı.

ODSO'nun kullanımı kötü belgelenmiştir ve bu nesnenin özelliklerini nasıl kullanacağınızı öğrenmenin en iyi yolu, istenen bir veri kaynağıyla bir belgeyi Microsoft Word'de manuel olarak oluşturup ardından bu belgeyi Aspose.Words ile açarak [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/) ve [Odso](../mailmergesettings/get_odso/) nesnelerinin özelliklerini incelemektir. Bu, örneğin bir veri kaynağını programlı olarak yapılandırmayı öğrenmek istediğinizde iyi bir yaklaşımdır.

Bu sınıfın nesnelerini doğrudan oluşturmanız genellikle gerekmez çünkü ODSO ayarları her zaman [Odso](../mailmergesettings/get_odso/) özelliği aracılığıyla kullanılabilir.

## Ayrıca Bakınız

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
