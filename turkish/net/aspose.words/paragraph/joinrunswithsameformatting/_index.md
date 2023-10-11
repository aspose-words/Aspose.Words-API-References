---
title: Paragraph.JoinRunsWithSameFormatting
second_title: Aspose.Words for .NET API Referansı
description: Paragraph yöntem. Birleştirmeler paragrafta aynı biçimlendirmeyle çalışır.
type: docs
weight: 300
url: /tr/net/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph.JoinRunsWithSameFormatting method

Birleştirmeler paragrafta aynı biçimlendirmeyle çalışır.

```csharp
public int JoinRunsWithSameFormatting()
```

### Geri dönüş değeri

Gerçekleştirilen birleştirme sayısı. Ne zaman **N** bitişik koşular birleştiriliyor, sayılırlar **N - 1** katıldı.

### Örnekler

Gereksiz çalıştırmaları birleştirerek paragrafların nasıl basitleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Paragrafa dört metin dizisi ekleyin.
builder.Write("Run 1. ");
builder.Write("Run 2. ");
builder.Write("Run 3. ");
builder.Write("Run 4. ");

// Bu belgeyi Microsoft Word'de açarsak paragraf kesintisiz bir metin gövdesi gibi görünecektir.
// Ancak aynı formatta dört ayrı çalıştırmadan oluşacaktır. Bunun gibi parçalanmış paragraflar
// Microsoft Word'de bir paragrafın bazı kısımlarını elle birçok kez düzenlediğimizde ortaya çıkabilir.
Paragraph para = builder.CurrentParagraph;

Assert.AreEqual(4, para.Runs.Count);

// Son çalıştırmanın stilini ilk üçten farklı olacak şekilde değiştirin.
para.Runs[3].Font.StyleIdentifier = StyleIdentifier.Emphasis;

// Belgenin içeriğini optimize etmek için "JoinRunsWithSameFormatting" yöntemini çalıştırabiliriz
// benzer işlemleri tek bir işlemde birleştirerek genel sayılarını azaltırız.
// Bu yöntem aynı zamanda bu yöntemin birleştirdiği çalıştırma sayısını da döndürür.
// Bu iki birleştirme İşlem #1, #2 ve #3'ü birleştirmek için gerçekleşti,
// uyumsuz bir stile sahip olduğundan 4. Çalıştırmayı dışarıda bırakırken.
Assert.AreEqual(2, para.JoinRunsWithSameFormatting());

// Kalan çalıştırma sayısı orijinal sayıya eşit olacak
// eksi "JoinRunsWithSameFormatting" yönteminin gerçekleştirdiği çalıştırma birleştirmelerinin sayısı.
Assert.AreEqual(2, para.Runs.Count);
Assert.AreEqual("Run 1. Run 2. Run 3. ", para.Runs[0].Text);
Assert.AreEqual("Run 4. ", para.Runs[1].Text);
```

### Ayrıca bakınız

* class [Paragraph](../)
* ad alanı [Aspose.Words](../../paragraph/)
* toplantı [Aspose.Words](../../../)


