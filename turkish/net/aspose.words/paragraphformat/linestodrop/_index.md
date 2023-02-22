---
title: ParagraphFormat.LinesToDrop
second_title: Aspose.Words for .NET API Referansı
description: ParagraphFormat mülk. Gömme yüksekliğini hesaplamak için kullanılan paragraf metninin satır sayısını alır veya ayarlar.
type: docs
weight: 200
url: /tr/net/aspose.words/paragraphformat/linestodrop/
---
## ParagraphFormat.LinesToDrop property

Gömme yüksekliğini hesaplamak için kullanılan paragraf metninin satır sayısını alır veya ayarlar.

```csharp
public int LinesToDrop { get; set; }
```

### Örnekler

Gömme boyutunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir paragrafı büyük harf olarak atamak için "LinesToDrop" özelliğini değiştirin,
// sonraki paragrafı süsleyecek büyük bir büyük harfe dönüştürecek.
// Gömmeye dört metin satırının yüksekliğini vermek için bu özelliğe 4 değerini verin.
builder.ParagraphFormat.LinesToDrop = 4;
builder.Writeln("H");

// Sonraki paragrafı sıradan bir paragrafa dönüştürmek için "LinesToDrop" özelliğini 0'a sıfırlayın.
// Bu paragraftaki metin, büyük ilk harfin etrafına sarılacaktır.
builder.ParagraphFormat.LinesToDrop = 0;
builder.Writeln("ello world!");

doc.Save(ArtifactsDir + "ParagraphFormat.LinesToDrop.odt");
```

### Ayrıca bakınız

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../paragraphformat/)
* toplantı [Aspose.Words](../../../)


