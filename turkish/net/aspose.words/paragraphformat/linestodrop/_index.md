---
title: ParagraphFormat.LinesToDrop
linktitle: LinesToDrop
articleTitle: LinesToDrop
second_title: Aspose.Words for .NET
description: ParagraphFormat LinesToDrop mülk. Gömme yüksekliğini hesaplamak için kullanılan paragraf metninin satır sayısını alır veya ayarlar C#'da.
type: docs
weight: 210
url: /tr/net/aspose.words/paragraphformat/linestodrop/
---
## ParagraphFormat.LinesToDrop property

Gömme yüksekliğini hesaplamak için kullanılan paragraf metninin satır sayısını alır veya ayarlar.

```csharp
public int LinesToDrop { get; set; }
```

## Örnekler

Gömme boyutunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir paragrafı büyük harf olarak atamak için "LinesToDrop" özelliğini değiştirin,
// bu onu bir sonraki paragrafı süsleyecek büyük bir büyük harfe dönüştürecek.
// Gömmeye dört metin satırının yüksekliğini vermek için bu özelliğe 4 değeri verin.
builder.ParagraphFormat.LinesToDrop = 4;
builder.Writeln("H");

// Sonraki paragrafı sıradan bir paragrafa dönüştürmek için "LinesToDrop" özelliğini 0'a sıfırlayın.
// Bu paragraftaki metin büyük harfin çevresine sarılacaktır.
builder.ParagraphFormat.LinesToDrop = 0;
builder.Writeln("ello world!");

doc.Save(ArtifactsDir + "ParagraphFormat.LinesToDrop.odt");
```

### Ayrıca bakınız

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
