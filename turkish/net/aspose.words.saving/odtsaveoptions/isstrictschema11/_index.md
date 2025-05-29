---
title: OdtSaveOptions.IsStrictSchema11
linktitle: IsStrictSchema11
articleTitle: IsStrictSchema11
second_title: .NET için Aspose.Words
description: ODT dışa aktarımlarınızı IsStrictSchema11 özelliğiyle optimize edin. En iyi sonuçlar için ODT 1.1 ile sıkı uyumluluğu sağlayın veya 1.2 uyumluluğunu etkinleştirin.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/odtsaveoptions/isstrictschema11/
---
## OdtSaveOptions.IsStrictSchema11 property

Dışa aktarma işleminin kesinlikle ODT 1.1 spesifikasyonuna uyup uymayacağını belirtir. OOo 3.0, dosyaları ODT 1.2 öğelerini ve özniteliklerini içerdiğinde doğru şekilde görüntüler. Bu amaçla "false" veya 1.1 spesifikasyonuna kesinlikle uymak için "true" kullanın. Varsayılan değer şudur:`YANLIŞ` .

```csharp
public bool IsStrictSchema11 { get; set; }
```

## Örnekler

Kaydedilmiş bir belgenin eski bir ODT şemasına uygun hale getirilmesinin nasıl yapılacağını gösterir.

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
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
