---
title: "Aspose::Words::Settings::MailMergeSettings sınıfı"
linktitle: "MailMergeSettings"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::MailMergeSettings sınıfı. Bir belge için tüm posta birleştirme bilgilerini belirtir. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class


Bir belge için tüm posta birleştirme bilgilerini belirtir. Daha fazla bilgi için, [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) dokümantasyon makalesini ziyaret edin.

```cpp
class MailMergeSettings : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Clear](./clear/)() | Belge kaydedildiğinde posta birleştirme ayarları kaydedilmez ve belge normal bir belge olur şekilde posta birleştirme ayarlarını temizler. |
| [Clone](./clone/)() | Bu nesnenin derin bir kopyasını döndürür. |
| [get_ActiveRecord](./get_activerecord/)() const | Microsoft Word'de görüntülenecek veri kaynağından kaydın bir‑tabanlı indeksini belirtir. Varsayılan değer 1'dir. |
| [get_AddressFieldName](./get_addressfieldname/)() const | Veri kaynağında e‑posta adreslerini içeren sütunu belirtir. Varsayılan değer boş bir dizedir. |
| [get_CheckErrors](./get_checkerrors/)() const | Posta birleştirme sırasında Microsoft Word tarafından yürütülecek hata raporlama türünü belirtir. Varsayılan değer [Default](../mailmergecheckerrors/). |
| [get_ConnectString](./get_connectstring/)() const | Harici bir veri kaynağına bağlanmak için kullanılan bağlantı dizesini belirtir. Varsayılan değer boş bir dizedir. |
| [get_DataSource](./get_datasource/)() const | Posta birleştirme veri kaynağının yolunu belirtir. Varsayılan değer boş bir dizedir. |
| [get_DataType](./get_datatype/)() const | Posta birleştirme veri kaynağının türünü ve veri erişim yöntemini belirtir. Varsayılan değer [Default](../mailmergedatatype/). |
| [get_Destination](./get_destination/)() const | Microsoft Word'ün posta birleştirme sonuçlarını nasıl çıkartacağını belirtir. Varsayılan değer [Default](../mailmergedestination/). |
| [get_DoNotSupressBlankLines](./get_donotsupressblanklines/)() const | Posta birleştirme yapan bir uygulamanın, posta birleştirme sonucunda oluşan birleştirilmiş belgelerdeki boş satırları nasıl işleyeceğini belirtir. Varsayılan değer **false**. |
| [get_HeaderSource](./get_headersource/)() const | Posta birleştirme başlık kaynağının yolunu belirtir. Varsayılan değer boş bir dizedir. |
| [get_LinkToQuery](./get_linktoquery/)() const | Bu konuda emin değilim. Microsoft Word Automation Reference, bunun sorgunun Microsoft Word'de belge her açıldığında çalıştırıldığını belirttiğini öne sürüyor. Ancak OOXML spesifikasyonu, bunun sorgunun gerçek sorguyu içeren harici bir sorgu dosyasına referans içerdiğini belirttiğini öne sürüyor. Varsayılan değer **false**. |
| [get_MailAsAttachment](./get_mailasattachment/)() const | Posta birleştirme işlemi sırasında üretilen belgelerin gerçek e‑postanın gövdesi yerine ek olarak e‑postalanması gerektiğini belirtir. Varsayılan değer **false**. |
| [get_MailSubject](./get_mailsubject/)() const | Posta birleştirme sırasında üretilen e‑postaların veya faksların konu satırında görünecek metni belirtir. Varsayılan değer boş bir dizedir. |
| [get_MainDocumentType](./get_maindocumenttype/)() const | Posta birleştirme ana belge türünü belirtir. Varsayılan değer [Default](../mailmergemaindocumenttype/). |
| [get_Odso](./get_odso/)() const | Office Data Source Object (ODSO) ayarlarını belirten nesneyi alır. |
| [get_Query](./get_query/)() const | Posta birleştirme işlemi gerçekleştirildiğinde belgeye içe aktarılacak kayıt kümesini döndürmek için belirtilen harici veri kaynağına karşı çalıştırılacak Structured Query Language (SQL) dizesini içerir. Varsayılan değer boş bir dizedir. |
| [get_ViewMergedData](./get_viewmergeddata/)() const | Microsoft Word'ün birleştirme alanlarının eklendiği (ör. birleştirilmiş verinin önizlemesi) belirtilen harici veri kaynağının verilerini görüntülemesi gerektiğini belirtir. Varsayılan değer **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MailMergeSettings](./mailmergesettings/)() |  |
| [set_ActiveRecord](./set_activerecord/)(int32_t) | Microsoft Word'de görüntülenecek veri kaynağından kaydın bir‑tabanlı indeksini belirtir. Varsayılan değer 1'dir. |
| [set_AddressFieldName](./set_addressfieldname/)(const System::String\&) | Veri kaynağında e‑posta adreslerini içeren sütunu belirtir. Varsayılan değer boş bir dizedir. |
| [set_CheckErrors](./set_checkerrors/)(Aspose::Words::Settings::MailMergeCheckErrors) | Posta birleştirme sırasında Microsoft Word tarafından yürütülecek hata raporlama türünü belirtir. Varsayılan değer [Default](../mailmergecheckerrors/). |
| [set_ConnectString](./set_connectstring/)(const System::String\&) | Harici bir veri kaynağına bağlanmak için kullanılan bağlantı dizesini belirtir. Varsayılan değer boş bir dizedir. |
| [set_DataSource](./set_datasource/)(const System::String\&) | Posta birleştirme veri kaynağının yolunu belirtir. Varsayılan değer boş bir dizedir. |
| [set_DataType](./set_datatype/)(Aspose::Words::Settings::MailMergeDataType) | Posta birleştirme veri kaynağının türünü ve veri erişim yöntemini belirtir. Varsayılan değer [Default](../mailmergedatatype/). |
| [set_Destination](./set_destination/)(Aspose::Words::Settings::MailMergeDestination) | Microsoft Word'ün posta birleştirme sonuçlarını nasıl çıkartacağını belirtir. Varsayılan değer [Default](../mailmergedestination/). |
| [set_DoNotSupressBlankLines](./set_donotsupressblanklines/)(bool) | Posta birleştirme yapan bir uygulamanın, posta birleştirme sonucunda oluşan birleştirilmiş belgelerdeki boş satırları nasıl işleyeceğini belirtir. Varsayılan değer **false**. |
| [set_HeaderSource](./set_headersource/)(const System::String\&) | Posta birleştirme başlık kaynağının yolunu belirtir. Varsayılan değer boş bir dizedir. |
| [set_LinkToQuery](./set_linktoquery/)(bool) | [Aspose::Words::Settings::MailMergeSettings::get_LinkToQuery](./get_linktoquery/) için ayarlayıcı. |
| [set_MailAsAttachment](./set_mailasattachment/)(bool) | Posta birleştirme işlemi sırasında üretilen belgelerin gerçek e‑postanın gövdesi yerine ek olarak e‑postalanması gerektiğini belirtir. Varsayılan değer **false**. |
| [set_MailSubject](./set_mailsubject/)(const System::String\&) | Posta birleştirme sırasında üretilen e‑postaların veya faksların konu satırında görünecek metni belirtir. Varsayılan değer boş bir dizedir. |
| [set_MainDocumentType](./set_maindocumenttype/)(Aspose::Words::Settings::MailMergeMainDocumentType) | [Aspose::Words::Settings::MailMergeSettings::get_MainDocumentType](./get_maindocumenttype/) için ayarlayıcı. |
| [set_Odso](./set_odso/)(const System::SharedPtr\<Aspose::Words::Settings::Odso\>\&) | Office Data Source Object (ODSO) ayarlarını belirten nesneyi ayarlar. |
| [set_Query](./set_query/)(const System::String\&) | Posta birleştirme işlemi gerçekleştirildiğinde belgeye içe aktarılacak kayıt kümesini döndürmek için belirtilen harici veri kaynağına karşı çalıştırılacak Structured Query Language (SQL) dizesini içerir. Varsayılan değer boş bir dizedir. |
| [set_ViewMergedData](./set_viewmergeddata/)(bool) | Microsoft Word'ün birleştirme alanlarının eklendiği (ör. birleştirilmiş verinin önizlemesi) belirtilen harici veri kaynağının verilerini görüntülemesi gerektiğini belirtir. Varsayılan değer **false**. |
| static [Type](./type/)() |  |
## Açıklamalar


Bu nesneyi bir belge için posta birleştirme veri kaynağını belirtmek için kullanabilirsiniz; bu bilgi (mevcut veri alanlarıyla birlikte) kullanıcı bu belgeyi açtığında Microsoft Word'de görünür. Ya da bu nesneyi, kullanıcının bu belge için Microsoft Word'de belirttiği posta birleştirme ayarlarını sorgulamak için kullanabilirsiniz.

Bu sınıfın nesnelerini doğrudan oluşturmanız genellikle gerekli değildir çünkü bir belgenin posta birleştirme ayarları her zaman [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/) özelliği aracılığıyla kullanılabilir.

Bu belgenin bir posta birleştirme ana belgesi olup olmadığını tespit etmek için, [MainDocumentType](./get_maindocumenttype/) özelliğinin değerini kontrol edin.

Bir belgeden posta birleştirme ayarlarını ve veri kaynağı bilgilerini kaldırmak için [Clear](./clear/) yöntemini kullanabilirsiniz. Aspose.Words, [MainDocumentType](./get_maindocumenttype/) özelliği [NotAMergeDocument](../mailmergemaindocumenttype/) olarak ayarlanmışsa veya [DataType](./get_datatype/) özelliği [None](../mailmergedatatype/) olarak ayarlanmışsa posta birleştirme ayarlarını belgeye yazmaz.

Bu nesnenin özelliklerini nasıl kullanacağınızı öğrenmenin en iyi yolu, istenen bir veri kaynağıyla bir belgeyi Microsoft Word'de manuel olarak oluşturup ardından o belgeyi Aspose.Words ile açarak [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/) ve [Odso](./get_odso/) nesnelerinin özelliklerini incelemektir. Örneğin, bir veri kaynağını programlı olarak yapılandırmayı öğrenmek istiyorsanız bu iyi bir yaklaşımdır.

Aspose.Words, belgeleri farklı formatlar arasında yüklerken, kaydederken ve dönüştürürken posta birleştirme bilgilerini korur, ancak kendi posta birleştirmesini [MailMerge](../../aspose.words.mailmerging/mailmerge/) nesnesiyle gerçekleştirirken bu bilgileri kullanmaz.

## Ayrıca Bakınız

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
