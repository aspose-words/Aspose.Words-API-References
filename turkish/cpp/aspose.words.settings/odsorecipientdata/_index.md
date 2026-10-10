---
title: "Aspose::Words::Settings::OdsoRecipientData sınıfı"
linktitle: "OdsoRecipientData"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::OdsoRecipientData sınıfı. Tek bir kaydın dış veri kaynağındaki bilgilerini temsil eder ve bu kayıt posta birleştirmesinden hariç tutulur. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.settings/odsorecipientdata/
---
## OdsoRecipientData class


Posta birleştirmeden hariç tutulacak harici veri kaynağındaki tek bir kayda ait bilgileri temsil eder. Daha fazla bilgi için, [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) dokümantasyon makalesini ziyaret edin.

```cpp
class OdsoRecipientData : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Clone](./clone/)() | Bu nesnenin derin bir kopyasını döndürür. |
| [get_Active](./get_active/)() const | Veri kaynağından gelen kaydın posta birleştirmesi yapıldığında bir belgeye aktarılıp aktarılmayacağını belirtir. Varsayılan değer **true**'dur. |
| [get_Column](./get_column/)() const | Mevcut kayıt için benzersiz verileri içeren veri kaynağındaki sütunu belirtir. Varsayılan değer 0'dır. |
| [get_Hash](./get_hash/)() const | Bu kaydın karma kodunu temsil eder. Bazen Microsoft Word, bir [Hash](./get_hash/) değerini, bir [UniqueTag](./get_uniquetag/) değerinin yerine tüm kayıt için kullanır. Varsayılan değer 0'dır. |
| [get_UniqueTag](./get_uniquetag/)() const | Benzersiz veri içeren sütunda verilen kaydın içeriğini belirtir. Varsayılan değer **null**'dır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OdsoRecipientData](./odsorecipientdata/)() |  |
| [set_Active](./set_active/)(bool) | Veri kaynağından gelen kaydın posta birleştirmesi yapıldığında bir belgeye aktarılıp aktarılmayacağını belirtir. Varsayılan değer **true**'dur. |
| [set_Column](./set_column/)(int32_t) | Mevcut kayıt için benzersiz verileri içeren veri kaynağındaki sütunu belirtir. Varsayılan değer 0'dır. |
| [set_Hash](./set_hash/)(int32_t) | Bu kaydın karma kodunu temsil eder. Bazen Microsoft Word, bir [Hash](./get_hash/) değerini, bir [UniqueTag](./get_uniquetag/) değerinin yerine tüm kayıt için kullanır. Varsayılan değer 0'dır. |
| [set_UniqueTag](./set_uniquetag/)(const System::ArrayPtr\<uint8_t\>\&) | Benzersiz veri içeren sütunda verilen kaydın içeriğini belirtir. Varsayılan değer **null**'dır. |
| static [Type](./type/)() |  |
## Açıklamalar


Bir kayıt birleştirilmiş bir belgeye birleştirilecekse, o kayıt hakkında bilgi gerekmez. Ancak, belirli bir kayıt birleştirilmiş bir belgeye birleştirilmeyecekse, bu kaydın benzersiz anahtarının değeri, bu nesnenin [UniqueTag](./get_uniquetag/) özelliğinde saklanarak bu dışlamayı gösterir.
## Ayrıca Bakınız

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
