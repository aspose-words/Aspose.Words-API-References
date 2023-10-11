---
title: Document.JoinRunsWithSameFormatting
second_title: Aspose.Words for .NET API Referansı
description: Document yöntem. Birleştirmeler belgenin tüm paragraflarında aynı formatta çalışır.
type: docs
weight: 640
url: /tr/net/aspose.words/document/joinrunswithsameformatting/
---
## Document.JoinRunsWithSameFormatting method

Birleştirmeler belgenin tüm paragraflarında aynı formatta çalışır.

```csharp
public int JoinRunsWithSameFormatting()
```

### Geri dönüş değeri

Gerçekleştirilen birleştirme sayısı. Ne zaman **N** bitişik koşular birleştiriliyor, sayılırlar **N - 1** katıldı.

### Notlar

Bu bir optimizasyon yöntemidir. Bazı belgeler aynı biçimlendirmeye sahip bitişik çalışmalar içerir. Genellikle bu, bir belge yoğun bir şekilde manuel olarak düzenlendiyse meydana gelir. Bu işlemleri birleştirerek belge boyutunu küçültebilir ve daha sonraki işlemleri hızlandırabilirsiniz.

Operasyon her şeyi kontrol ediyor[`Paragraph`](../../paragraph/) bitişik için belgedeki düğüm[`Run`](../../run/) düğümleri aynı özelliklere sahip. run oluşturma ve değiştirme düzenleme oturumlarını izlemek için kullanılan benzersiz tanımlayıcıları yok sayar. Her birleştirme sırasındaki ilk çalıştırma tüm metni biriktirir. Remaining çalıştırmalar belgeden silinir.

### Örnekler

Gereksiz çalıştırmaları azaltmak için bir belgede çalıştırmaların nasıl birleştirileceğini gösterir.

```csharp
// Aynı biçimlendirmeye sahip bitişik metin dizilerini içeren bir belge açın,
// Microsoft Word'de aynı paragrafı birden çok kez düzenlediğimizde sıklıkla ortaya çıkar.
Document doc = new Document(MyDir + "Rendering.docx");

// Bu çalıştırmalardan herhangi biri aynı biçimlendirmeyle bitişikse,
// o zaman belge basitleştirilebilir.
Assert.AreEqual(317, doc.GetChildNodes(NodeType.Run, true).Count);

// Bu tür çalıştırmaları bu yöntemle birleştirin ve gerçekleşecek çalıştırma birleştirme sayısını doğrulayın.
Assert.AreEqual(121, doc.JoinRunsWithSameFormatting());

// Birleştirme sayısı ve birleştirme sonrasında sahip olduğumuz çalıştırma sayısı
// başlangıçta yaptığımız çalıştırma sayısını toplamalıyız.
Assert.AreEqual(196, doc.GetChildNodes(NodeType.Run, true).Count);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


