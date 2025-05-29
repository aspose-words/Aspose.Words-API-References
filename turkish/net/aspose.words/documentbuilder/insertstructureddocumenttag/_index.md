---
title: DocumentBuilder.InsertStructuredDocumentTag
linktitle: InsertStructuredDocumentTag
articleTitle: InsertStructuredDocumentTag
second_title: .NET için Aspose.Words
description: DocumentBuilder InsertStructuredDocumentTag yöntemiyle belgelerinizi zahmetsizce geliştirin. Daha iyi organizasyon için yapılandırılmış belge etiketlerini kolayca ekleyin!
type: docs
weight: 480
url: /tr/net/aspose.words/documentbuilder/insertstructureddocumenttag/
---
## DocumentBuilder.InsertStructuredDocumentTag method

Bir ekler[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) belgeye.

```csharp
public StructuredDocumentTag InsertStructuredDocumentTag(SdtType type)
```

### Geri dönüş değeri

The[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) yeni eklenen düğüm.

## Örnekler

Yapılandırılmış belge etiketinin nasıl kolayca ekleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveTo(doc.FirstSection.Body.Paragraphs[3]);
// Yalnızca aşağıdaki StructuredDocumentTag türlerinin eklenmesine izin verildiğini unutmayın:
// SdtType.PlainText, SdtType.RichText, SdtType.Onay Kutusu, SdtType.Açılır Liste,
// SdtType.ComboBox, SdtType.Resim, SdtType.Tarih.
// Eklenen StructuredDocumentTag'in işaretleme düzeyi otomatik olarak algılanacak ve eklenecek konuma bağlı olacaktır.
// StructuredDocumentTag eklendi, paragraf ve yazı tipi biçimlendirmesini imleç konumundan devralacak.
StructuredDocumentTag sdtPlain = builder.InsertStructuredDocumentTag(SdtType.PlainText);

doc.Save(ArtifactsDir + "StructuredDocumentTag.InsertStructuredDocumentTag.docx");
```

### Ayrıca bakınız

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* enum [SdtType](../../../aspose.words.markup/sdttype/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
