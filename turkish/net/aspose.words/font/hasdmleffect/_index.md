---
title: Font.HasDmlEffect
linktitle: HasDmlEffect
articleTitle: HasDmlEffect
second_title: .NET için Aspose.Words
description: Belirli bir DrawingML metin efektinin Font HasDmlEffect yöntemi ile uygulanıp uygulanmadığını keşfedin. Belgenizin görsel çekiciliğini zahmetsizce artırın!
type: docs
weight: 570
url: /tr/net/aspose.words/font/hasdmleffect/
---
## Font.HasDmlEffect method

Belirli DrawingML metin efektinin uygulanıp uygulanmadığını kontrol eder.

```csharp
public bool HasDmlEffect(TextDmlEffect dmlEffectType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| dmlEffectType | TextDmlEffect | DrawingML metin efekti türü. |

### Geri dönüş değeri

`doğru` eğer belirli DrawingML metin efekti uygulanırsa.

## Örnekler

Bir çalışmanın DrawingML metin efekti gösterip göstermediğinin nasıl kontrol edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "DrawingML text effects.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.True(runs[0].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[1].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[2].Font.HasDmlEffect(TextDmlEffect.Reflection));
Assert.True(runs[3].Font.HasDmlEffect(TextDmlEffect.Effect3D));
Assert.True(runs[4].Font.HasDmlEffect(TextDmlEffect.Fill));
```

### Ayrıca bakınız

* enum [TextDmlEffect](../../textdmleffect/)
* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
