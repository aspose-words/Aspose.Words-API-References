---
title: Document.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: .NET için Aspose.Words
description: JoinRunsWithSameFormatting yönteminin, belgenizin paragraflarındaki biçimlendirilmiş metni kusursuz bir şekilde birleştirerek cilalı, profesyonel bir görünüm elde etmesinin nasıl sağlandığını keşfedin.
type: docs
weight: 660
url: /tr/net/aspose.words/document/joinrunswithsameformatting/
---
## Document.JoinRunsWithSameFormatting method

Belgenin tüm paragraflarında aynı biçimlendirmeyle çalışmaları birleştirir.

```csharp
public int JoinRunsWithSameFormatting()
```

### Geri dönüş değeri

Gerçekleştirilen birleştirme sayısı.**N** bitişik koşular birleştirildiğinde bunlar sayılır**N - 1** katılır.

## Notlar

Bu bir optimizasyon yöntemidir. Bazı belgeler aynı biçimlendirmeye sahip bitişik çalıştırmalar içerir. Genellikle bu, bir belge yoğun bir şekilde manuel olarak düzenlendiğinde meydana gelir. Bu çalıştırmaları birleştirerek belge boyutunu küçültebilir ve daha fazla işlemeyi hızlandırabilirsiniz.

İşlem her şeyi kontrol eder[`Paragraph`](../../paragraph/) belgedeki bitişik düğüm[`Run`](../../run/)Aynı özelliklere sahip düğümleri. run oluşturma ve değiştirme düzenleme oturumlarını izlemek için kullanılan benzersiz tanımlayıcıları yok sayar. Her birleştirme dizisindeki ilk çalıştırma tüm metni biriktirir. Kalan çalıştırmalar belgeden silinir.

## Örnekler

Gereksiz çalıştırmaları azaltmak için bir belgedeki çalıştırmaların nasıl birleştirileceğini gösterir.

```csharp
// Aynı biçimlendirmeye sahip bitişik metin dizilerini içeren bir belgeyi açın,
// Microsoft Word'de aynı paragrafı birden fazla düzenlediğimizde sıklıkla karşılaşılan bir durumdur.
Document doc = new Document(MyDir + "Rendering.docx");

// Bu çalıştırmaların herhangi bir sayısı aynı biçimlendirmeyle bitişikse,
// o zaman belge basitleştirilebilir.
Assert.AreEqual(317, doc.GetChildNodes(NodeType.Run, true).Count);

// Bu tür çalıştırmaları bu yöntemle birleştir ve gerçekleşecek çalıştırma katılımlarının sayısını doğrula.
Assert.AreEqual(121, doc.JoinRunsWithSameFormatting());

// Join sayısı ve join sonrasında sahip olduğumuz çalıştırma sayısı
// başlangıçta yaptığımız koşuların sayısını toplamalıyız.
Assert.AreEqual(196, doc.GetChildNodes(NodeType.Run, true).Count);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
