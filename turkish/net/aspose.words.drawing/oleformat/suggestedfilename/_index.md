---
title: OleFormat.SuggestedFileName
second_title: Aspose.Words for .NET API Referansı
description: OleFormat mülk. Geçerli gömülü nesneyi bir dosyaya kaydetmek istiyorsanız önerilen dosya adını alır.
type: docs
weight: 130
url: /tr/net/aspose.words.drawing/oleformat/suggestedfilename/
---
## OleFormat.SuggestedFileName property

Geçerli gömülü nesneyi bir dosyaya kaydetmek istiyorsanız, önerilen dosya adını alır.

```csharp
public string SuggestedFileName { get; }
```

### Örnekler

Bir OLE nesnesinin önerilen dosya adının nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "OLE shape.rtf");

Shape oleShape = (Shape) doc.FirstSection.Body.GetChild(NodeType.Shape, 0, true);

// OLE nesneleri önerilen bir dosya adı ve uzantısı sağlayabilir,
// bunu nesnenin içeriğini yerel dosya sistemindeki bir dosyaya kaydederken kullanabiliriz.
string suggestedFileName = oleShape.OleFormat.SuggestedFileName;

Assert.AreEqual("CSV.csv", suggestedFileName);

using (FileStream fileStream = new FileStream(ArtifactsDir + suggestedFileName, FileMode.Create))
{
    oleShape.OleFormat.Save(fileStream);
}
```

### Ayrıca bakınız

* class [OleFormat](../)
* ad alanı [Aspose.Words.Drawing](../../oleformat/)
* toplantı [Aspose.Words](../../../)


