---
title: "Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource yöntemi"
linktitle: "GetDataSource"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource yöntemi. Aspose.Words birleştirme motoru, C++'ta üst düzey bir birleştirme bölgesi başlangıcıyla karşılaştığında bu yöntemi çağırır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/
---
## IMailMergeDataSourceRoot::GetDataSource method


Aspose.Words birleştirme motoru, üst düzey bir birleştirme bölgesinin başlangıcına rastladığında bu yöntemi çağırır.

```cpp
virtual System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource(System::String tableName)=0
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tableName | System::String | Şablon belgesinde belirtilen posta birleştirme bölgesi adı. Büyük/küçük harfe duyarsız. |

### ReturnValue

Belirtilen tablonun veri kayıtlarına erişim sağlayacak bir veri kaynağı nesnesi.
## Açıklamalar


Aspose.Words birleştirme motorları bir belgeyi veriyle doldururken MERGEFIELD TableStart:TableName ile karşılaştığında, bu nesnede [GetDataSource()](./) yöntemini çağırır. Uygulamanız yeni bir veri kaynağı nesnesi döndürmelidir. Aspose.Words, birleştirme bölgesini doldurmak için döndürülen veri kaynağını kullanacaktır.

Belirtilen adla bir veri kaynağı (tablo) mevcut değilse, uygulamanız **null** döndürmelidir.

## Ayrıca Bakınız

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Interface [IMailMergeDataSourceRoot](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
