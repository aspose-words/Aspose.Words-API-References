---
title: StructuredDocumentTag.LockContents
linktitle: LockContents
articleTitle: LockContents
second_title: Aspose.Words for .NET
description: StructuredDocumentTag LockContents mülk. Olarak ayarlandığındadoğru  bu özellik kullanıcının bu içeriği düzenlemesini yasaklarSDT  C#'da.
type: docs
weight: 200
url: /tr/net/aspose.words.markup/structureddocumenttag/lockcontents/
---
## StructuredDocumentTag.LockContents property

Olarak ayarlandığında`doğru` , bu özellik kullanıcının bu içeriği düzenlemesini yasaklar**SDT** .

```csharp
public bool LockContents { get; set; }
```

## Örnekler

Yapılandırılmış belge etiketlerine düzenleme kısıtlamalarının nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Kullanıcının onu doldurmasını isteyen bir metin kutusu görevi gören, düz metin yapılı bir belge etiketi ekleyin.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Kullanıcının bu metin kutusunun içeriğini düzenlemesini engellemek için "LockContents" özelliğini "true" olarak ayarlayın.
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Kullanıcının şunları yapmasını engellemek için "LockContentControl" özelliğini "true" olarak ayarlayın
// bu yapılandırılmış belge etiketinin Microsoft Word'de manuel olarak silinmesi.
tag.LockContentControl = true;

builder.InsertParagraph();
builder.Write("This structured document tag cannot be deleted but its contents can be edited: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Lock.docx");
```

### Ayrıca bakınız

* class [StructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
