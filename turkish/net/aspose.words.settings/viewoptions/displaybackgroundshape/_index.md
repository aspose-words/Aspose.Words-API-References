---
title: ViewOptions.DisplayBackgroundShape
linktitle: DisplayBackgroundShape
articleTitle: DisplayBackgroundShape
second_title: Aspose.Words for .NET
description: ViewOptions DisplayBackgroundShape mülk. Yazdırma düzeni görünümünde arka plan şeklinin görüntülenmesini kontrol eder C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.settings/viewoptions/displaybackgroundshape/
---
## ViewOptions.DisplayBackgroundShape property

Yazdırma düzeni görünümünde arka plan şeklinin görüntülenmesini kontrol eder.

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

// Belgenin kaynağının düz renkli bir arka planı var,
// bunun varlığı "DisplayBackgroundShape" bayrağını "true" olarak ayarlayacaktır.
Assert.True(doc.ViewOptions.DisplayBackgroundShape);

// Belgenin arka plan rengini göstermesini sağlamak için "DisplayBackgroundShape" değerini "true" olarak tutun.
// Bu, görünürlüğü artırmak için bazı metin renklerini etkileyebilir.
// Arka plan rengini göstermemek için "DisplayBackgroundShape" değerini "false" olarak ayarlayın.
doc.ViewOptions.DisplayBackgroundShape = displayBackgroundShape;

doc.Save(ArtifactsDir + "ViewOptions.DisplayBackgroundShape.docx");
```

### Ayrıca bakınız

* class [ViewOptions](../)
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
