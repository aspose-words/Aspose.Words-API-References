---
title: ViewOptions.DisplayBackgroundShape
second_title: Aspose.Words for .NET API Referansı
description: ViewOptions mülk. Baskı düzeni görünümünde arka plan şeklinin görüntüsünü kontrol eder.
type: docs
weight: 10
url: /tr/net/aspose.words.settings/viewoptions/displaybackgroundshape/
---
## ViewOptions.DisplayBackgroundShape property

Baskı düzeni görünümünde arka plan şeklinin görüntüsünü kontrol eder.

```csharp
public bool DisplayBackgroundShape { get; set; }
```

### Örnekler

Görünüm seçeneklerinde belge arka plan görüntülerinin nasıl gizleneceğini/gösterileceğini gösterir.

```csharp
// Düz bir arka plan rengine sahip yeni bir belge oluşturmak için bir HTML dizesi kullanın.
const string html = 
@"<html>
    <body style='background-color: blue'>
        <p>Hello world!</p>
    </body>
</html>";

Document doc = new Document(new MemoryStream(Encoding.Unicode.GetBytes(html)));

// Belgenin kaynağı düz renkli bir arka plana sahip,
// varlığı "DisplayBackgroundShape" bayrağını "true" olarak ayarlayacaktır.
Assert.True(doc.ViewOptions.DisplayBackgroundShape);

// Belgenin arka plan rengini görüntülemesini sağlamak için "DisplayBackgroundShape"i "true" olarak tutun.
// Bu, görünürlüğü artırmak için bazı metin renklerini etkileyebilir.
// Arka plan rengini göstermemek için "DisplayBackgroundShape"i "false" olarak ayarlayın.
doc.ViewOptions.DisplayBackgroundShape = displayBackgroundShape;

doc.Save(ArtifactsDir + "ViewOptions.DisplayBackgroundShape.docx");
```

### Ayrıca bakınız

* class [ViewOptions](../)
* ad alanı [Aspose.Words.Settings](../../viewoptions/)
* toplantı [Aspose.Words](../../../)


