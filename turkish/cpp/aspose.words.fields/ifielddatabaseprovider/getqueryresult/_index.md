---
title: "Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult yöntemi"
linktitle: "GetQueryResult"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult yöntemi. C++'ta sorgu sonucunu döndürür."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/ifielddatabaseprovider/getqueryresult/
---
## IFieldDatabaseProvider::GetQueryResult method


Sorgu sonucunu döndürür.

```cpp
virtual System::SharedPtr<Aspose::Words::Fields::FieldDatabaseDataTable> Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult(System::String fileName, System::String connection, System::String query, System::SharedPtr<Aspose::Words::Fields::FieldDatabase> field)=0
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | System::String | \d alan anahtarında belirtilen veritabanının tam yolu ve dosya adı. |
| connection | System::String | \c alan anahtarında belirtilen veriye bağlantı. |
| sorgu | System::String | SQL komutları kümesi, \s alan anahtarında belirtilen veritabanını sorgular. |
| field | System::SharedPtr\<Aspose::Words::Fields::FieldDatabase\> | Güncellenen alan. |

### ReturnValue

Alan güncellemesi için kullanılacak [FieldDatabaseDataTable](../../fielddatabasedatatable/) örneği.

## Ayrıca Bakınız

* Class [FieldDatabaseDataTable](../../fielddatabasedatatable/)
* Class [FieldDatabase](../../fielddatabase/)
* Interface [IFieldDatabaseProvider](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
