---
title: OleFormat.SuggestedFileName
linktitle: SuggestedFileName
articleTitle: SuggestedFileName
second_title: .NET için Aspose.Words
description: Gömülü nesnelerinizi sorunsuz bir şekilde kaydetmek için önerilen dosya adını kolayca almak amacıyla OleFormat SuggestedFileName özelliğini keşfedin.
type: docs
weight: 130
url: /tr/net/aspose.words.drawing/oleformat/suggestedfilename/
---
## OleFormat.SuggestedFileName property

Mevcut gömülü nesneyi bir dosyaya kaydetmek istiyorsanız, nesne için önerilen dosya adını alır.

```csharp
public string SuggestedFileName { get; }
```

## Örnekler

Bir OLE nesnesinin önerilen dosya adının nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "OLE shape.rtf");

Shape oleShape = (Shape)doc.FirstSection.Body.GetChild(NodeType.Shape, 0, true);

// OLE nesneleri önerilen bir dosya adı ve uzantı sağlayabilir,
// yerel dosya sistemindeki bir dosyaya nesnenin içeriğini kaydederken kullanabiliriz.
string suggestedFileName = oleShape.OleFormat.SuggestedFileName;

Assert.AreEqual("CSV.csv", suggestedFileName);

using (FileStream fileStream = new FileStream(ArtifactsDir + suggestedFileName, FileMode.Create))
{
    oleShape.OleFormat.Save(fileStream);
}
```

### Ayrıca bakınız

* class [OleFormat](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
