---
title: "Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource yöntemi"
linktitle: "GetChildDataSource"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource yöntemi. Aspose.Words posta birleştirme motoru, C++'ta iç içe bir posta birleştirme bölgesi başlangıcıyla karşılaştığında bu yöntemi çağırır."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource::GetChildDataSource method


Aspose.Words posta birleştirme motoru, iç içe bir posta birleştirme bölgesi başlangıcına rastladığında bu yöntemi çağırır.

```cpp
virtual System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource(System::String tableName)=0
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tableName | System::String | Şablon belgesinde belirtilen posta birleştirme bölgesi adı. Büyük/küçük harfe duyarsız. |

### ReturnValue

Belirtilen tablonun veri kayıtlarına erişim sağlayacak bir veri kaynağı nesnesi.
## Açıklamalar


Aspose.Words posta birleştirme motorları bir posta birleştirme bölgesini veriyle doldururken ve MERGEFIELD TableStart:TableName biçiminde iç içe bir posta birleştirme bölgesi başlangıcıyla karşılaştığında, mevcut veri kaynağı nesnesinde [GetChildDataSource()](./) yöntemini çağırır. Uygulamanız, mevcut üst kaydın alt kayıtlarına erişim sağlayacak yeni bir veri kaynağı nesnesi döndürmelidir. Aspose.Words, döndürülen veri kaynağını iç içe posta birleştirme bölgesini doldurmak için kullanacaktır.

Aşağıda [GetChildDataSource()](./) uygulamasının uyması gereken kurallar verilmiştir.

Bu veri kaynağı nesnesi tarafından temsil edilen tablonun belirtilen ada sahip ilişkili bir alt (detay) tablosu varsa, uygulamanız mevcut kaydın alt kayıtlarına erişim sağlayacak yeni bir [IMailMergeDataSource](../) nesnesi döndürmelidir. Buna bir örnek Orders / OrderDetails ilişkisidir. Mevcut [IMailMergeDataSource](../) nesnesinin Orders tablosunu temsil ettiğini ve mevcut bir sipariş kaydına sahip olduğunu varsayalım. Sonra Aspose.Words belgede "MERGEFIELD TableStart:OrderDetails" ile karşılaşır ve [GetChildDataSource()](./) yöntemini çağırır. Aspose.Words'un mevcut sipariş için OrderDetails kaydına erişebilmesi için bir [IMailMergeDataSource](../) nesnesi oluşturup döndürmeniz gerekir.

Bu veri kaynağı nesnesinin belirtilen ada sahip tabloyla bir ilişkisi yoksa, belirtilen tablonun tüm kayıtlarına erişim sağlayacak bir [IMailMergeDataSource](../) nesnesi döndürmeniz gerekir.

Belirtilen ada sahip bir tablo mevcut değilse, uygulamanız **null** döndürmelidir.

## Ayrıca Bakınız

* Interface [IMailMergeDataSource](../)
* Interface [IMailMergeDataSource](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
