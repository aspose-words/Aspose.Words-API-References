---
title: ReportingEngine.UseReflectionOptimization
linktitle: UseReflectionOptimization
articleTitle: UseReflectionOptimization
second_title: .NET için Aspose.Words
description: ReportingEngine'in UseReflectionOptimization özelliği ile özel tip üye çağrılarını optimize edin. Daha iyi verimlilik için dinamik sınıf oluşturma ile performansı artırın.
type: docs
weight: 60
url: /tr/net/aspose.words.reporting/reportingengine/usereflectionoptimization/
---
## ReportingEngine.UseReflectionOptimization property

Yansıma API'si aracılığıyla gerçekleştirilen özel tür üyelerinin çağrılarının dinamik sınıf oluşturma kullanılarak optimize edilip edilmediğini belirten bir değer alır veya ayarlar. Varsayılan değer`doğru` .

```csharp
public static bool UseReflectionOptimization { get; set; }
```

## Notlar

Bu optimizasyonu devre dışı bırakmanın tercih edildiği bazı senaryolar vardır. Örneğin, sürekli olarak küçük veri öğeleri koleksiyonlarıyla uğraşıyorsanız, dinamik sınıf oluşturmanın yükü doğrudan yansıma API çağrılarının yükünden daha belirgin olabilir. Bu seçenek iOS'ta çalıştırıldığında ve yansıma optimizasyonu kullanılmadığında etkili olmaz.

### Ayrıca bakınız

* class [ReportingEngine](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)
