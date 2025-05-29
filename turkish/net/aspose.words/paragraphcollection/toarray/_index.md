---
title: ParagraphCollection.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: .NET için Aspose.Words
description: ToArray yöntemi ile ParagraphCollection'ınızı zahmetsizce bir diziye dönüştürerek veri yönetimini kolaylaştırın ve belge işlemenizi geliştirin.
type: docs
weight: 20
url: /tr/net/aspose.words/paragraphcollection/toarray/
---
## ParagraphCollection.ToArray method

Koleksiyondaki tüm paragrafları yeni bir paragraf dizisine kopyalar.

```csharp
public Paragraph[] ToArray()
```

### Geri dönüş değeri

Bir dizi paragraf.

## Örnekler

NodeCollection'dan bir dizinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

Paragraph[] paras = doc.FirstSection.Body.Paragraphs.ToArray();

Assert.AreEqual(22, paras.Length);
```

Numaralandırma sırasında bir düğümü kaldırmak için "sıcak kaldırma"nın nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("The first paragraph");
builder.Writeln("The second paragraph");
builder.Writeln("The third paragraph");
builder.Writeln("The fourth paragraph");

// Bir numaralandırmanın ortasındaki koleksiyondan bir düğümü kaldır.
foreach (Paragraph para in doc.FirstSection.Body.Paragraphs.ToArray())
    if (para.Range.Text.Contains("third"))
        para.Remove();

Assert.False(doc.GetText().Contains("The third paragraph"));
```

### Ayrıca bakınız

* class [Paragraph](../../paragraph/)
* class [ParagraphCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
