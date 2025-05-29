---
title: ParagraphFormat.LinesToDrop
linktitle: LinesToDrop
articleTitle: LinesToDrop
second_title: .NET için Aspose.Words
description: ParagraphFormat LinesToDrop özelliğinin belgelerinizdeki büyük harf yüksekliğini nasıl geliştirdiğini keşfedin. Çarpıcı görseller için metin düzeninizi optimize edin!
type: docs
weight: 210
url: /tr/net/aspose.words/paragraphformat/linestodrop/
---
## ParagraphFormat.LinesToDrop property

Büyük harf yüksekliğini hesaplamak için kullanılan paragraf metninin satır sayısını alır veya ayarlar.

```csharp
public int LinesToDrop { get; set; }
```

## Örnekler

Büyük harf boyutunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir paragrafı büyük harfle belirtmek için "LinesToDrop" özelliğini değiştirin,
// bu da onu bir sonraki paragrafı süsleyecek büyük bir büyük harfe dönüştürecektir.
// Bu özelliğe 4 değerini vererek büyük harfin dört metin satırının yüksekliğini verin.
builder.ParagraphFormat.LinesToDrop = 4;
builder.Writeln("H");

// Bir sonraki paragrafı sıradan bir paragrafa dönüştürmek için "LinesToDrop" özelliğini 0'a sıfırlayın.
// Bu paragraftaki metin büyük harfin etrafına sarılacaktır.
builder.ParagraphFormat.LinesToDrop = 0;
builder.Writeln("ello world!");

doc.Save(ArtifactsDir + "ParagraphFormat.LinesToDrop.odt");
```

### Ayrıca bakınız

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
