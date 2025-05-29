---
title: Paragraph.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: .NET için Aspose.Words
description: JoinRunsWithSameFormatting metodunu kullanarak paragraflarınızdaki tutarlı biçimlendirmeyle zahmetsizce birleştirin. Belgenizin stilini bugün geliştirin!
type: docs
weight: 300
url: /tr/net/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph.JoinRunsWithSameFormatting method

Paragraftaki aynı biçimlendirmeyle koşuları birleştirir.

```csharp
public int JoinRunsWithSameFormatting()
```

### Geri dönüş değeri

Gerçekleştirilen birleştirme sayısı.**N** bitişik koşular birleştirildiğinde bunlar sayılır**N - 1** katılır.

## Örnekler

Gereksiz paragrafları birleştirerek paragrafların nasıl basitleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Paragrafa dört metin parçası ekle.
builder.Write("Run 1. ");
builder.Write("Run 2. ");
builder.Write("Run 3. ");
builder.Write("Run 4. ");

// Bu belgeyi Microsoft Word'de açarsak paragraf tek bir metin gövdesi gibi görünecektir.
// Ancak, aynı biçimlendirmeye sahip dört ayrı çalışmadan oluşacaktır. Bunun gibi parçalanmış paragraflar
// Microsoft Word'de bir paragrafın bölümlerini birçok kez elle düzenlediğimizde ortaya çıkabilir.
Paragraph para = builder.CurrentParagraph;

Assert.AreEqual(4, para.Runs.Count);

// Son çalışmanın stilini ilk üçünden farklı kılmak için değiştir.
para.Runs[3].Font.StyleIdentifier = StyleIdentifier.Emphasis;

// Belgenin içeriğini optimize etmek için "JoinRunsWithSameFormatting" metodunu çalıştırabiliriz
// benzer koşuları tek bir koşuda birleştirerek toplam sayılarını azaltır.
// Bu metot aynı zamanda bu metodun birleştirdiği çalıştırma sayısını da döndürür.
// Bu iki birleştirme, 1, 2 ve 3 numaralı koşuları birleştirmek için gerçekleşti.
// 4. Çalıştırma'yı uyumsuz bir stile sahip olduğu için dışarıda bıraktık.
Assert.AreEqual(2, para.JoinRunsWithSameFormatting());

// Kalan koşu sayısı orijinal sayıya eşit olacaktır
// "JoinRunsWithSameFormatting" yönteminin gerçekleştirdiği çalıştırma birleştirmelerinin sayısı çıkarılır.
Assert.AreEqual(2, para.Runs.Count);
Assert.AreEqual("Run 1. Run 2. Run 3. ", para.Runs[0].Text);
Assert.AreEqual("Run 4. ", para.Runs[1].Text);
```

### Ayrıca bakınız

* class [Paragraph](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
