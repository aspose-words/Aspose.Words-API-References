---
title: StructuredDocumentTag.LockContents
second_title: Aspose.Words for .NET API Referansı
description: StructuredDocumentTag mülk. true olarak ayarlandığında bu özellik bir kullanıcının bunun içeriğini düzenlemesini engeller. SDT .
type: docs
weight: 200
url: /tr/net/aspose.words.markup/structureddocumenttag/lockcontents/
---
## StructuredDocumentTag.LockContents property

true olarak ayarlandığında, bu özellik bir kullanıcının bunun içeriğini düzenlemesini engeller. **SDT** .

```csharp
public bool LockContents { get; set; }
```

### Örnekler

Yapılandırılmış belge etiketlerine düzenleme kısıtlamalarının nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Kullanıcıdan onu doldurmasını isteyen bir metin kutusu görevi gören düz metin yapılandırılmış bir belge etiketi ekleyin.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Kullanıcının bu metin kutusunun içeriğini düzenlemesini engellemek için "LockContents" özelliğini "true" olarak ayarlayın.
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// "LockContentControl" özelliğini, kullanıcının
// bu yapılandırılmış belge etiketini Microsoft Word'de manuel olarak silme.
tag.LockContentControl = true;

builder.InsertParagraph();
builder.Write("This structured document tag cannot be deleted but its contents can be edited: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Lock.docx");
```

### Ayrıca bakınız

* class [StructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../structureddocumenttag/)
* toplantı [Aspose.Words](../../../)


