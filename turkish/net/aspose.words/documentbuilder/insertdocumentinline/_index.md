---
title: DocumentBuilder.InsertDocumentInline
linktitle: InsertDocumentInline
articleTitle: InsertDocumentInline
second_title: .NET için Aspose.Words
description: DocumentBuilder InsertDocumentInline yöntemiyle belgeleri zahmetsizce satır içi olarak ekleyin, iş akışınızı ve belge düzenleme deneyiminizi geliştirin.
type: docs
weight: 320
url: /tr/net/aspose.words/documentbuilder/insertdocumentinline/
---
## DocumentBuilder.InsertDocumentInline method

İmleç konumuna satır içi bir belge ekler.

```csharp
public Node InsertDocumentInline(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcDoc | Document | Ekleme için kaynak belge. |
| importFormatMode | ImportFormatMode | Çakışan stil biçimlendirmesinin nasıl birleştirileceğini belirtir. |
| importFormatOptions | ImportFormatOptions | Sonuç belgesinin biçimlendirmesini etkileyen seçeneklerin belirlenmesine olanak tanır. |

### Geri dönüş değeri

Eklenen içeriğin ilk düğümü.

## Notlar

Bu yöntem, MS Word davranışını taklit eder; sanki CTRL+'A' (tüm içeriği seç) tuşlarına basılmış gibi, sonra bir belgenin içinde CTRL+'C' (seçili içeriği arabelleğe kopyala) tuşlarına basılıyor ve sonra başka bir belgenin içinde CTRL+'V' (arabellekten içerik ekle) tuşlarına basılıyor.

Fark olarak[`InsertDocument`](../insertdocument/) bu yöntem, kaynak belgenin eklendiği hedef belgenin paragrafının içeriğini, kaynak belgenin son paragrafına taşır. Aslında bu, son eklenen paragrafın paragraf sonunun kaldırıldığı anlamına gelir.

Dikkat, kaynak belgenin son düğümü bir paragraf değilse hiçbir şey yapılmayacaktır.

## Örnekler

İmleç konumuna satır içi bir belgenin nasıl ekleneceğini gösterir.

```csharp
DocumentBuilder srcDoc = new DocumentBuilder();
srcDoc.Write("[src content]");

// Hedef belgeyi oluştur.
DocumentBuilder dstDoc = new DocumentBuilder();
dstDoc.Write("Before ");
dstDoc.InsertNode(new BookmarkStart(dstDoc.Document, "src_place"));
dstDoc.InsertNode(new BookmarkEnd(dstDoc.Document, "src_place"));
dstDoc.Write(" after");

Assert.AreEqual("Before  after", dstDoc.Document.GetText().TrimEnd());

// Kaynak belgeyi hedef belgeye satır içi olarak ekle.
dstDoc.MoveToBookmark("src_place");
dstDoc.InsertDocumentInline(srcDoc.Document, ImportFormatMode.UseDestinationStyles, new ImportFormatOptions());

Assert.AreEqual("Before [src content] after", dstDoc.Document.GetText().TrimEnd());
```

### Ayrıca bakınız

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
