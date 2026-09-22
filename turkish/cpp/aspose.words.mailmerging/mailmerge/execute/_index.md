---
title: "Aspose::Words::MailMerging::MailMerge::Execute metodu"
linktitle: "Yürüt"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::MailMerging::MailMerge::Execute metodu. C++'ta tek bir kayıt için posta birleştirme işlemi gerçekleştirir."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.mailmerging/mailmerge/execute/
---
## MailMerge::Execute(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) method


Tek bir kayıt için posta birleştirme işlemi gerçekleştirir.

```cpp
void Aspose::Words::MailMerging::MailMerge::Execute(const System::ArrayPtr<System::String> &fieldNames, const System::ArrayPtr<System::SharedPtr<System::Object>> &values)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldNames | const System::ArrayPtr\<System::String\>\& | Birleştirme alanı adlarının dizisi. Alan adları büyük/küçük harfe duyarlı değildir. Belge içinde bulunamayan bir alan adıyla karşılaşıldığında, yok sayılır. |
| values | const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\& | Birleştirme alanlarına eklenecek değerlerin dizisi. Bu dizideki öğe sayısı *fieldNames* içindeki öğe sayısı ile aynı olmalıdır. |
## Açıklamalar


Bu metodu, belgedeki posta birleştirme alanlarını nesne dizisinden gelen değerlerle doldurmak için kullanın.

Bu metod yalnızca tek bir kayıt için verileri birleştirir. Alan adı dizisi ve değer dizisi tek bir kaydın verilerini temsil eder.

Bu metod posta birleştirme bölgelerini kullanmaz.

Bu metod, [RemoveUnusedRegions](../../mailmergecleanupoptions/) seçeneğini yok sayar.

## Örnekler



Bir URI'dan gelen bir resmi posta birleştirme verisi olarak MERGEFIELD içine nasıl birleştirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// \"Image:\" etiketli MERGEFIELD'ler posta birleştirme sırasında bir resim alacaktır.
// \"Image:\" etiketindeki iki nokta üstünden sonraki dize bir sütun adına karşılık gelir
// veri kaynağında, hücreleri resim dosyalarının URI'larını içeren.
builder->InsertField(u"MERGEFIELD  Image:logo_FromWeb ");
builder->InsertField(u"MERGEFIELD  Image:logo_FromFileSystem ");

// Birleştireceğimiz resimlerin URI'larını içeren bir veri kaynağı oluşturun.
// Bir URI, bir resme işaret eden bir web URL'si veya yerel dosya sistemindeki bir resim dosyasının dosya adı olabilir.
System::ArrayPtr<System::String> columns = System::MakeArray<System::String>({u"logo_FromWeb", u"logo_FromFileSystem"});
System::ArrayPtr<System::SharedPtr<System::Object>> URIs = System::MakeArray<System::SharedPtr<System::Object>>({System::ExplicitCast<System::Object>(get_ImageUrl()), System::ExplicitCast<System::Object>(get_ImageDir() + u"Logo.jpg")});

// Bir satır içeren veri kaynağı üzerinde bir posta birleştirme yürütün.
doc->get_MailMerge()->Execute(columns, URIs);

doc->Save(get_ArtifactsDir() + u"MailMergeEvent.ImageFromUrl.docx");
```

## Ayrıca Bakınız

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::Execute(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) method


Özel bir veri kaynağından posta birleştirme gerçekleştirir.

```cpp
void Aspose::Words::MailMerging::MailMerge::Execute(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> &dataSource)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dataSource | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\& | Özel posta birleştirme veri kaynağı arayüzünü uygulayan bir nesne. |
## Açıklamalar


Bu yöntemi, belge içindeki posta birleştirme alanlarını bir liste, hashtable veya nesneler gibi herhangi bir veri kaynağından gelen değerlerle doldurmak için kullanın. [IMailMergeDataSource](../../imailmergedatasource/) arayüzünü uygulayan kendi sınıfınızı yazmanız gerekir.

Bu yöntemi yalnızca [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) **false** olduğunda kullanabilirsiniz; yani Sağdan Sola (örneğin Arapça veya İbranice) dil uyumluluğuna ihtiyacınız yoktur.

Bu metod, [RemoveUnusedRegions](../../mailmergecleanupoptions/) seçeneğini yok sayar.

## Ayrıca Bakınız

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
