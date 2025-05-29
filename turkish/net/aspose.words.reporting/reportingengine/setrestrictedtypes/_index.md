---
title: ReportingEngine.SetRestrictedTypes
linktitle: SetRestrictedTypes
articleTitle: SetRestrictedTypes
second_title: .NET için Aspose.Words
description: ReportingEngine'deki SetRestrictedTypes yönteminin, optimize edilmiş veri raporlaması için şablon sözdiziminde üye erişimini sınırlayarak güvenliği nasıl artırdığını keşfedin.
type: docs
weight: 80
url: /tr/net/aspose.words.reporting/reportingengine/setrestrictedtypes/
---
## ReportingEngine.SetRestrictedTypes method

Şablon sözdizimi aracılığıyla engine tarafından hangi üyelerin ve hangi türetilmiş türlerin üyelerinin erişilemez olması gerektiğini belirtir.

```csharp
public static void SetRestrictedTypes(params Type[] types)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| types | Type[] | Kısıtlanacak tipler. |

## Notlar

Kısıtlı türler, bir raporun ilk oluşturulmasından önce ayarlanmalıdır. Sonrasında`Oluşturma Raporu` çağrıldığında, kısıtlı türler değiştirilemez ve bunu yapmaya çalışıldığında bir istisna atılır . Kısıtlı türleri ayarlamak için en iyi yer uygulama başlangıcıdır.

Çok sayıda kısıtlı türün performansı etkileyebileceğini unutmayın, bu nedenle yalnızca erişimi gerçekten hassas olan üyelerin olduğu türlerini kısıtlamak daha iyidir.

AtışlarArgumentException Aşağıdaki durumlarda:

-*types* boştur.

- Bir tanesi*types* öğeler`hükümsüz`.

- Bir tanesi*types* items görünmez bir türü, yani genel olmayan bir türü veya genel olmayan bir dış türe sahip genel bir iç içe türü temsil eder.

- Bir tanesi*types* items bir dizi türünü temsil eder.

-*types* yinelenen girdiler içeriyor.

## Örnekler

Güvenli kabul edilmeyen türdeki üyelere erişimin nasıl reddedileceğini gösterir.

```csharp
Document doc =
    DocumentHelper.CreateSimpleDocument(
        "<<var [typeVar = \"\".GetType().BaseType]>><<[typeVar]>>");

// Rapor oluştururken veya oluşturduktan sonra kısıtlı türler ayarlayamayacağınızı unutmayın.
ReportingEngine.SetRestrictedTypes(typeof(System.Type));
// Rapor oluştururken istisnaların yaşanmaması için "AllowMissingMembers" seçeneğini ayarladık.
ReportingEngine engine = new ReportingEngine() { Options = ReportBuildOptions.AllowMissingMembers };
engine.BuildReport(doc, new object());

// GetType() metoduna erişemediğimiz için boş bir dize alıyoruz.
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### Ayrıca bakınız

* class [ReportingEngine](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)
