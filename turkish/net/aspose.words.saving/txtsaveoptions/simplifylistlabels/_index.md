---
title: TxtSaveOptions.SimplifyListLabels
linktitle: SimplifyListLabels
articleTitle: SimplifyListLabels
second_title: .NET için Aspose.Words
description: TxtSaveOptions'ın SimplifyListLabels özelliğinin, karmaşık liste etiketlerini düzenleyerek metin gösterimini iyileştirerek anlaşılırlığı nasıl artırdığını keşfedin.
type: docs
weight: 70
url: /tr/net/aspose.words.saving/txtsaveoptions/simplifylistlabels/
---
## TxtSaveOptions.SimplifyListLabels property

Programın, karmaşık etiket biçimlendirmesinin düz metinle yeterince temsil edilmemesi durumunda liste etiketlerini basitleştirip basitleştirmeyeceğini belirtir.

Eğer ayarlanırsa`doğru` , numaralandırılmış liste etiketleri basit sayısal format olarak yazılır ve maddeler halinde liste etiketleri basit ASCII karakterleri olarak yazılır. Varsayılan değer`YANLIŞ`.

```csharp
public bool SimplifyListLabels { get; set; }
```

## Örnekler

Bir belgeyi düz metne kaydederken listelerin görünümünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Beş düzeyde girintiye sahip madde işaretli bir liste oluşturun.
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent();
builder.Writeln("Item 3");
builder.ListFormat.ListIndent();
builder.Writeln("Item 4");
builder.ListFormat.ListIndent();
builder.Write("Item 5");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "TxtSaveOptions" nesnesi oluşturun
// Belgeyi düz metne nasıl kaydedeceğimizi değiştirmek için.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Bazı listeleri dönüştürmek için "SimplifyListLabels" özelliğini "true" olarak ayarlayın
// sembolleri daha basit ASCII karakterlerine dönüştürüyoruz, örneğin '*', 'o', '+', '>', vb.
// Mümkün olduğunca çok sayıda orijinal liste sembolünü korumak için "SimplifyListLabels" özelliğini "false" olarak ayarlayın.
txtSaveOptions.SimplifyListLabels = simplifyListLabels;

doc.Save(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt");

string newLine = Environment.NewLine;

if (simplifyListLabels)
    Assert.AreEqual($"* Item 1{newLine}" +
                    $"  > Item 2{newLine}" +
                    $"    + Item 3{newLine}" +
                    $"      - Item 4{newLine}" +
                    $"        o Item 5{newLine}", docText);
else
    Assert.AreEqual($"· Item 1{newLine}" +
                    $"o Item 2{newLine}" +
                    $"§ Item 3{newLine}" +
                    $"· Item 4{newLine}" +
                    $"o Item 5{newLine}", docText);
```

### Ayrıca bakınız

* class [TxtSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
