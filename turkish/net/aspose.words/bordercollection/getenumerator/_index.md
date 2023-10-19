---
title: BorderCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words for .NET
description: BorderCollection GetEnumerator yöntem. Koleksiyondaki tüm kenarlıklar üzerinde yineleme yapmak için kullanılabilecek bir numaralandırıcı nesnesini döndürür C#'da.
type: docs
weight: 160
url: /tr/net/aspose.words/bordercollection/getenumerator/
---
## BorderCollection.GetEnumerator method

Koleksiyondaki tüm kenarlıklar üzerinde yineleme yapmak için kullanılabilecek bir numaralandırıcı nesnesini döndürür.

```csharp
public IEnumerator<Border> GetEnumerator()
```

## Örnekler

Bir paragraf formatı nesnesindeki tüm kenarlıkların nasıl yineleneceğini ve düzenleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Her tarafta yeşil dalga kenarlığı oluşturmak için oluşturucunun paragraf formatı ayarlarını yapılandırın.
BorderCollection borders = builder.ParagraphFormat.Borders;

using (IEnumerator<Border> enumerator = borders.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Border border = enumerator.Current;
        border.Color = Color.Green;
        border.LineStyle = LineStyle.Wave;
        border.LineWidth = 3;
    }
}

// Bir paragraf ekleyin. Kenarlık ayarlarımız, kenarlığının görünümünü belirleyecektir.
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "BorderCollection.GetBordersEnumerator.docx");
```

### Ayrıca bakınız

* class [Border](../../border/)
* class [BorderCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
