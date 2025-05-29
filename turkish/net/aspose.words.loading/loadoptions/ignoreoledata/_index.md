---
title: LoadOptions.IgnoreOleData
linktitle: IgnoreOleData
articleTitle: IgnoreOleData
second_title: .NET için Aspose.Words
description: LoadOptions IgnoreOleData özelliğinin OLE veri işlemeyi kontrol etmenize izin vererek veri işlemenizi nasıl geliştirdiğini keşfedin. İş akışınızı bugün optimize edin!
type: docs
weight: 70
url: /tr/net/aspose.words.loading/loadoptions/ignoreoledata/
---
## LoadOptions.IgnoreOleData property

OLE verilerinin yoksayılıp yoksayılmayacağını belirtir.

```csharp
public bool IgnoreOleData { get; set; }
```

## Notlar

Hedef formatın OLE nesnelerini desteklemediği durumlarda OLE verilerinin göz ardı edilmesi, bellek tüketimini azaltabilir ve veri kaybı olmadan performansı artırabilir.

Varsayılan değer:`YANLIŞ`.

## Örnekler

Yükleme sırasında OLE verilerinin nasıl dikkate alınacağını gösterir.

```csharp
// OLE verilerinin göz ardı edilmesi bellek tüketimini azaltabilir ve performansı artırabilir
// hedef formatın OLE nesnelerini desteklememesi durumunda veri kaybı yaşanmaz.
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Document doc = new Document(MyDir + "OLE objects.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.IgnoreOleData.docx");
```

### Ayrıca bakınız

* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
