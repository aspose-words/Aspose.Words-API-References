---
title: ViewOptions.DisplayBackgroundShape
linktitle: DisplayBackgroundShape
articleTitle: DisplayBackgroundShape
second_title: .NET için Aspose.Words
description: Baskı düzeninizi, cilalı bir görünüm için özelleştirilebilir arka plan şekilleriyle geliştirmek üzere ViewOptions'daki DisplayBackgroundShape özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.settings/viewoptions/displaybackgroundshape/
---
## ViewOptions.DisplayBackgroundShape property

Baskı düzeni görünümünde arka plan şeklinin görüntüsünü kontrol eder.

```csharp
public bool DisplayBackgroundShape { get; set; }
```

## Örnekler

Görünüm seçeneklerinde belge arka plan resimlerinin nasıl gizleneceğini/görüntüleneceğini gösterir.

```csharp
// Düz arka plan rengine sahip yeni bir belge oluşturmak için bir HTML dizesi kullanın.
const string html = 
@"<html>
    <body style='background-color: blue'>
        <p>Hello world!</p>
    </body>
</html>";

Document doc = new Document(new MemoryStream(Encoding.Unicode.GetBytes(html)));

// Belgenin kaynağı düz renkli bir arka plana sahiptir,
// varlığı "DisplayBackgroundShape" bayrağını "true" olarak ayarlayacaktır.
Assert.True(doc.ViewOptions.DisplayBackgroundShape);

// Belgenin arka plan rengini göstermesi için "DisplayBackgroundShape" değerini "true" olarak tutun.
// Bu, görünürlüğü artırmak için bazı metin renklerini etkileyebilir.
// Arka plan rengini göstermemek için "DisplayBackgroundShape" değerini "false" olarak ayarlayın.
doc.ViewOptions.DisplayBackgroundShape = displayBackgroundShape;

doc.Save(ArtifactsDir + "ViewOptions.DisplayBackgroundShape.docx");
```

### Ayrıca bakınız

* class [ViewOptions](../)
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
