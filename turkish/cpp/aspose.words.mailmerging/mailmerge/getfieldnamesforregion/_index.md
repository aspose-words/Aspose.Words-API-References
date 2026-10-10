---
title: "Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion yöntemi"
linktitle: "GetFieldNamesForRegion"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion yöntemi. C++'ta bölgede mevcut olan posta birleştirme alan adlarının bir koleksiyonunu döndürür."
type: docs
weight: 22000
url: /tr/cpp/aspose.words.mailmerging/mailmerge/getfieldnamesforregion/
---
## MailMerge::GetFieldNamesForRegion(const System::String\&) method


Bölgede mevcut olan posta birleştirme alanı adlarının bir koleksiyonunu döndürür.

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion(const System::String &regionName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| regionName | const System::String\& | Bölge adı (büyük/küçük harfe duyarsız). |
## Açıklamalar


İsteğe bağlı önek dahil tam birleştirme alan adlarını döndürür. Yinelenen alan adlarını ortadan kaldırmaz.

Belge aynı ada sahip birden fazla bölge içeriyorsa, en ilk bölge işlenir.

Her çağrıda yeni bir dize dizisi oluşturulur.

## Ayrıca Bakınız

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::GetFieldNamesForRegion(const System::String\&, int32_t) method


Bölgede mevcut olan posta birleştirme alanı adlarının bir koleksiyonunu döndürür.

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion(const System::String &regionName, int32_t regionIndex)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| regionName | const System::String\& | Bölge adı (büyük/küçük harfe duyarsız). |
| regionIndex | int32_t | Bölge indeksi (sıfır tabanlı). |
## Açıklamalar


İsteğe bağlı önek dahil tam birleştirme alan adlarını döndürür. Yinelenen alan adlarını ortadan kaldırmaz.

Belge aynı ada sahip birden fazla bölge içeriyorsa, N'inci bölge (sıfır tabanlı) işlenir.

Her çağrıda yeni bir dize dizisi oluşturulur.

## Ayrıca Bakınız

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
