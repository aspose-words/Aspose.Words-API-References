---
title: OdtSaveOptions.IsStrictSchema11
second_title: Aspose.Words for .NET API Referansı
description: OdtSaveOptions mülk. Dışa aktarmanın ODT spesifikasyonu 1.1e tam olarak karşılık gelip gelmeyeceğini belirtir. OOo 3.0 ODT 1.2nin öğelerini ve niteliklerini içerdiğinde dosyaları doğru şekilde görüntüler. Bu amaç için yanlışı veya 1.1. spesifikasyonuna tam uygunluk için doğruyu kullanın. Varsayılan değerYANLIŞ .
type: docs
weight: 20
url: /tr/net/aspose.words.saving/odtsaveoptions/isstrictschema11/
---
## OdtSaveOptions.IsStrictSchema11 property

Dışa aktarmanın ODT spesifikasyonu 1.1'e tam olarak karşılık gelip gelmeyeceğini belirtir. OOo 3.0, ODT 1.2'nin öğelerini ve niteliklerini içerdiğinde dosyaları doğru şekilde görüntüler. Bu amaç için "yanlış"ı veya 1.1. spesifikasyonuna tam uygunluk için "doğru"yu kullanın. Varsayılan değer:`YANLIŞ` .

```csharp
public bool IsStrictSchema11 { get; set; }
```

### Örnekler

Kaydedilen bir belgenin eski bir ODT şemasına nasıl uygun hale getirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Ayrıca bakınız

* class [OdtSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../odtsaveoptions/)
* toplantı [Aspose.Words](../../../)


