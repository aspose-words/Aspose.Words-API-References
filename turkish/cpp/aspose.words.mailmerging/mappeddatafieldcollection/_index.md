---
title: "Aspose::Words::MailMerging::MappedDataFieldCollection sınıfı"
linktitle: "MappedDataFieldCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::MailMerging::MappedDataFieldCollection sınıfı. Veri kaynağınızdaki alan adları ile belgedeki posta birleştirme alanı adları arasında otomatik eşleme yapmanıza olanak tanır. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.mailmerging/mappeddatafieldcollection/
---
## MappedDataFieldCollection class


Veri kaynağınızdaki alan adları ile belgedeki posta birleştirme alan adları arasında otomatik eşleme yapmaya olanak tanır. Daha fazla bilgi için, [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) dokümantasyon makalesini ziyaret edin.

```cpp
class MappedDataFieldCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, System::String>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | Yeni bir alan eşlemesi ekler. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [ContainsKey](./containskey/)(const System::String\&) | Belgedeki belirtilen alandan bir eşlemenin koleksiyonda bulunup bulunmadığını belirler. |
| [ContainsValue](./containsvalue/)(const System::String\&) | Veri kaynağındaki belirtilen alandan bir eşlemenin koleksiyonda bulunup bulunmadığını belirler. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Koleksiyonda bulunan eleman sayısını alır. |
| [GetEnumerator](./getenumerator/)() override | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir sözlük enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Belirtilen posta birleştirme alanıyla ilişkili veri kaynağındaki alanın adını alır veya ayarlar. |
| [idx_set](./idx_set/)(const System::String\&, const System::String\&) | Belirtilen posta birleştirme alanıyla ilişkili veri kaynağındaki alanın adını alır veya ayarlar. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Bir alan eşlemesini kaldırır. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Açıklama |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Açıklamalar


Bu, dize anahtarlarının dize değerlerine dönüştürüldüğü bir koleksiyon olarak uygulanır. Anahtarlar, belgedeki posta birleştirme alanlarının adlarıdır ve değerler, veri kaynağınızdaki alanların adlarıdır.

## Ayrıca Bakınız

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
