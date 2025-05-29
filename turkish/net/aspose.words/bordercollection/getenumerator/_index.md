---
title: BorderCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: .NET için Aspose.Words
description: Tüm sınırlar arasında kolayca yineleme yapmak, kodlama verimliliğinizi ve koleksiyon yönetiminizi artırmak için BorderCollection GetEnumerator metodunu keşfedin.
type: docs
weight: 160
url: /tr/net/aspose.words/bordercollection/getenumerator/
---
## BorderCollection.GetEnumerator method

Koleksiyondaki tüm sınırlar üzerinde yineleme yapmak için kullanılabilecek bir numaratör nesnesi döndürür.

```csharp
public IEnumerator<Border> GetEnumerator()
```

## Örnekler

Bir paragraf biçim nesnesindeki tüm kenarlıklar üzerinde nasıl yineleme yapılacağını ve bunların nasıl düzenleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Oluşturucunun paragraf biçimi ayarlarını, her tarafta yeşil dalgalı bir kenarlık oluşturacak şekilde yapılandırın.
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
