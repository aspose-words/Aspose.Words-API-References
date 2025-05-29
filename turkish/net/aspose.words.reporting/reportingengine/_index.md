---
title: ReportingEngine Class
linktitle: ReportingEngine
articleTitle: ReportingEngine
second_title: .NET için Aspose.Words
description: Aspose.Words.ReportingEngine ile güçlü belge otomasyonunun kilidini açın. Şablonları verilerle kolayca doldurun ve sorunsuz raporlama için ayarları özelleştirin.
type: docs
weight: 5470
url: /tr/net/aspose.words.reporting/reportingengine/
---
## ReportingEngine class

Şablon belgelerini verilerle doldurmak için rutinler ve bu rutinleri kontrol etmek için bir dizi ayar sağlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[LINQ Raporlama Motoru](https://docs.aspose.com/words/net/linq-reporting-engine/) belgeleme makalesi.

```csharp
public class ReportingEngine
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [ReportingEngine](reportingengine/)() | Bu sınıfın yeni bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [KnownTypes](../../aspose.words.reporting/reportingengine/knowntypes/) { get; } | Aşağıdakileri içeren sıralanmamış bir küme (yani benzersiz öğelerden oluşan bir koleksiyon) alır:Type Bu engine örneği tarafından işlenen rapor şablonları içerisinde ilgili türlerin statik üyelerini çağırmak, tür dönüştürmeleri gerçekleştirmek vb. için tam veya kısmen nitelikli adları kullanılabilen nesneler |
| [MissingMemberMessage](../../aspose.words.reporting/reportingengine/missingmembermessage/) { get; set; } | Bir nesnenin eksik bir üyesine düz bir referansı temsil eden bir şablon ifadesi yerine yazdırılan bir dize değerini alır veya ayarlar. Varsayılan değer boş bir dizedir. |
| [Options](../../aspose.words.reporting/reportingengine/options/) { get; set; } | Bu davranışın kontrol edildiği bir bayrak kümesini alır veya ayarlar`ReportingEngine` Bir rapor oluştururken örneği. |
| static [UseReflectionOptimization](../../aspose.words.reporting/reportingengine/usereflectionoptimization/) { get; set; } | Yansıma API'si aracılığıyla gerçekleştirilen özel tür üyelerinin çağrılarının dinamik sınıf oluşturma kullanılarak optimize edilip edilmediğini belirten bir değer alır veya ayarlar. Varsayılan değer`doğru` . |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport)(*[Document](../../aspose.words/document/), object*) | Belirtilen şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve onu hazır bir rapor haline getirir. |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_1)(*[Document](../../aspose.words/document/), object, string*) | Belirtilen şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve onu hazır bir rapor haline getirir. |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_2)(*[Document](../../aspose.words/document/), object[], string[]*) | Belirtilen şablon belgesini belirtilen kaynaklardan gelen verilerle doldurarak hazır bir rapor haline getirir. |
| static [GetRestrictedTypes](../../aspose.words.reporting/reportingengine/getrestrictedtypes/)() | Türleri, hangi üyelerin ve hangi türetilmiş türlerin üyelerinin şablon sözdizimi aracılığıyla engine tarafından erişilemez olması gerektiğini döndürür. |
| static [SetRestrictedTypes](../../aspose.words.reporting/reportingengine/setrestrictedtypes/)(*params Type[]*) | Şablon sözdizimi aracılığıyla engine tarafından hangi üyelerin ve hangi türetilmiş türlerin üyelerinin erişilemez olması gerektiğini belirtir. |

### Ayrıca bakınız

* ad alanı [Aspose.Words.Reporting](../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../)
