---
title: "Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions yöntemi"
linktitle: "ExecuteWithRegions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions yöntemi. C++'ta özelleştirilmiş bir veri kaynağından ve posta birleştirme bölgeleriyle bir posta birleştirme gerçekleştirir."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.mailmerging/mailmerge/executewithregions/
---
## MailMerge::ExecuteWithRegions(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) method


Özel bir veri kaynağından posta birleştirme bölgeleriyle posta birleştirme gerçekleştirir.

```cpp
void Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> &dataSource)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dataSource | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\& | Özel posta birleştirme veri kaynağı arayüzünü uygulayan bir nesne. |
## Açıklamalar


Bu yöntemi, belge içindeki posta birleştirme alanlarını bir XML dosyası veya iş nesneleri koleksiyonları gibi herhangi bir özelleştirilmiş veri kaynağından gelen değerlerle doldurmak için kullanın. [IMailMergeDataSource](../../imailmergedatasource/) arayüzünü uygulayan kendi sınıfınızı yazmanız gerekir.

Bu yöntemi yalnızca [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) **false** olduğunda kullanabilirsiniz; yani Sağdan Sola (örneğin Arapça veya İbranice) dil uyumluluğuna ihtiyacınız yoktur.

## Ayrıca Bakınız

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::ExecuteWithRegions(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\&) method


Özel bir veri kaynağından posta birleştirme bölgeleriyle posta birleştirme gerçekleştirir.

```cpp
void Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSourceRoot> &dataSourceRoot)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dataSourceRoot | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\& | Özelleştirilmiş posta birleştirme veri kaynağı kök arayüzünü uygulayan bir nesne. |
## Açıklamalar


Bu yöntemi, belge içindeki posta birleştirme alanlarını bir XML dosyası veya iş nesneleri koleksiyonları gibi herhangi bir özelleştirilmiş veri kaynağından gelen değerlerle doldurmak için kullanın. [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/) ve [IMailMergeDataSource](../../imailmergedatasource/) arayüzlerini uygulayan kendi sınıflarınızı yazmanız gerekir.

Bu yöntemi yalnızca [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) **false** olduğunda kullanabilirsiniz; yani Sağdan Sola (örneğin Arapça veya İbranice) dil uyumluluğuna ihtiyacınız yoktur.

## Ayrıca Bakınız

* Interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
