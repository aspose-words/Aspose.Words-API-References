---
title: StructuredDocumentTag.IsTemporary
linktitle: IsTemporary
articleTitle: IsTemporary
second_title: .NET için Aspose.Words
description: StructuredDocumentTag IsTemporary özelliğinin, içerik değişiklikleri üzerine SDT'nizin WordProcessingML'den kaldırılıp kaldırılmayacağını nasıl belirlediğini keşfedin. Belgelerinizi bugün optimize edin!
type: docs
weight: 160
url: /tr/net/aspose.words.markup/structureddocumenttag/istemporary/
---
## StructuredDocumentTag.IsTemporary property

Bunun olup olmadığını belirtir**SDT** içerikleri değiştirildiğinde WordProcessingML belgesinden kaldırılacaktır.

```csharp
public bool IsTemporary { get; set; }
```

## Örnekler

Tek kullanımlık kontrollerin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document();

// Düz metin yapılandırılmış bir belge etiketi ekleyin,
// Kullanıcının metin girebileceği düz metin formu görevi görecektir.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Yapılandırılmış belge etiketinin kaybolması ve
// Kullanıcının Microsoft Word'de bir kez düzenlemesinin ardından içeriğini belgeye entegre eder.
// Kullanıcının içerikleri düzenlemesine izin vermek için "IsTemporary" özelliğini "false" olarak ayarlayın
// yapılandırılmış belge etiketinin herhangi bir sayıda.
tag.IsTemporary = isTemporary;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Please enter text: ");
builder.InsertNode(tag);

// Onay kutusu biçiminde başka bir yapılandırılmış belge etiketi ekleyin ve varsayılan durumunu "işaretli" olarak ayarlayın.
tag = new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline);
tag.Checked = true;

// Onay kutusunun bir sembole dönüşmesi için "IsTemporary" özelliğini "true" olarak ayarlayın
// Microsoft Word'de kullanıcı üzerine tıkladığında.
// Kullanıcının onay kutusuna istediği kadar tıklamasına izin vermek için "IsTemporary" özelliğini "false" olarak ayarlayın.
tag.IsTemporary = isTemporary;

builder.Write("\nPlease click the check box: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IsTemporary.docx");
```

### Ayrıca bakınız

* class [StructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
