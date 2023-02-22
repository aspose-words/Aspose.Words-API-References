---
title: TxtSaveOptions.SimplifyListLabels
second_title: Aspose.Words for .NET API Referansı
description: TxtSaveOptions mülk. Karmaşık etiket biçimlendirmesinin düz metinle yeterince temsil edilmemesi durumunda programın liste etiketlerini basitleştirmesi gerekip gerekmediğini belirtir.
type: docs
weight: 70
url: /tr/net/aspose.words.saving/txtsaveoptions/simplifylistlabels/
---
## TxtSaveOptions.SimplifyListLabels property

Karmaşık etiket biçimlendirmesinin düz metinle yeterince temsil edilmemesi durumunda programın liste etiketlerini basitleştirmesi gerekip gerekmediğini belirtir.

olarak ayarlanırsa **doğru** , numaralı liste etiketleri basit sayısal biçimde ve ayrıntılı liste etiketleri basit ASCII karakterleri olarak yazılır. Varsayılan değer **yanlış**.

```csharp
public bool SimplifyListLabels { get; set; }
```

### Örnekler

Bir belgeyi düz metne kaydederken listelerin görünümünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Beş düzey girintili madde işaretli bir liste oluşturun.
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

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "TxtSaveOptions" nesnesi oluşturun
// belgeyi düz metne kaydetme şeklimizi değiştirmek için.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Bazı listeleri dönüştürmek için "SimplifyListLabels" özelliğini "true" olarak ayarlayın
// sembolleri '*', 'o', '+', '>' vb. gibi daha basit ASCII karakterlerine dönüştürün.
// Mümkün olduğu kadar çok orijinal liste sembolünü korumak için "SimplifyListLabels" özelliğini "false" olarak ayarlayın.
txtSaveOptions.SimplifyListLabels = simplifyListLabels;

doc.Save(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt");

if (simplifyListLabels)
    Assert.AreEqual("* Item 1\r\n" +
                    "  > Item 2\r\n" +
                    "    + Item 3\r\n" +
                    "      - Item 4\r\n" +
                    "        o Item 5\r\n", docText);
else
    Assert.AreEqual("· Item 1\r\n" +
                    "o Item 2\r\n" +
                    "§ Item 3\r\n" +
                    "· Item 4\r\n" +
                    "o Item 5\r\n", docText);
```

### Ayrıca bakınız

* class [TxtSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../txtsaveoptions/)
* toplantı [Aspose.Words](../../../)


