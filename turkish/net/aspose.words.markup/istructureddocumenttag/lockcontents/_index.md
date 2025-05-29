---
title: IStructuredDocumentTag.LockContents
linktitle: LockContents
articleTitle: LockContents
second_title: .NET için Aspose.Words
description: IStructuredDocumentTag LockContents özelliğinin içerik düzenlemelerini önleyerek belge güvenliğini nasıl artırdığını keşfedin. SDT'nizin bozulmadan kaldığından emin olun!
type: docs
weight: 80
url: /tr/net/aspose.words.markup/istructureddocumenttag/lockcontents/
---
## IStructuredDocumentTag.LockContents property

Bu özellik doğru olarak ayarlandığında, kullanıcının bu içeriği düzenlemesini yasaklayacaktır.**SDT** .

```csharp
public bool LockContents { get; set; }
```

## Örnekler

Yapılandırılmış belge etiketlerine düzenleme kısıtlamalarının nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Kullanıcının doldurmasını isteyen bir metin kutusu görevi gören düz metin yapılandırılmış belge etiketi ekleyin.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Kullanıcının bu metin kutusunun içeriğini düzenlemesini engellemek için "LockContents" özelliğini "true" olarak ayarlayın.
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Kullanıcının bunu yapmasını engellemek için "LockContentControl" özelliğini "true" olarak ayarlayın
// Bu yapılandırılmış belge etiketini Microsoft Word'de manuel olarak siliyorum.
tag.LockContentControl = true;

builder.InsertParagraph();
builder.Write("This structured document tag cannot be deleted but its contents can be edited: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Lock.docx");
```

### Ayrıca bakınız

* interface [IStructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
