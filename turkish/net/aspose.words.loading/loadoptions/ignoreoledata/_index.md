---
title: LoadOptions.IgnoreOleData
second_title: Aspose.Words for .NET API Referansı
description: LoadOptions mülk. OLE verilerinin yoksayılıp yok sayılmayacağını belirtir.
type: docs
weight: 70
url: /tr/net/aspose.words.loading/loadoptions/ignoreoledata/
---
## LoadOptions.IgnoreOleData property

OLE verilerinin yoksayılıp yok sayılmayacağını belirtir.

```csharp
public bool IgnoreOleData { get; set; }
```

### Notlar

OLE verilerinin göz ardı edilmesi, bellek tüketimini azaltabilir ve hedef formatın OLE nesnelerini desteklemediği bir durumda veri kaybı olmadan performansı artırabilir.

Varsayılan değer:`YANLIŞ`.

### Örnekler

Yükleme sırasında OLE verilerinin nasıl alınacağını gösterir.

```csharp
// OLE verilerinin göz ardı edilmesi bellek tüketimini azaltabilir ve performansı artırabilir
// hedef formatın OLE nesnelerini desteklememesi durumunda veri kaybı olmadan.
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Document doc = new Document(MyDir + "OLE objects.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.IgnoreOleData.docx");
```

### Ayrıca bakınız

* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../loadoptions/)
* toplantı [Aspose.Words](../../../)


