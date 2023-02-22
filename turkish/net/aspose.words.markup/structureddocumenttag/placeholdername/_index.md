---
title: StructuredDocumentTag.PlaceholderName
second_title: Aspose.Words for .NET API Referansı
description: StructuredDocumentTag mülk. Adını alır veya ayarlarBuildingBlock yer tutucu metni içeren.
type: docs
weight: 240
url: /tr/net/aspose.words.markup/structureddocumenttag/placeholdername/
---
## StructuredDocumentTag.PlaceholderName property

Adını alır veya ayarlar[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/) yer tutucu metni içeren.

Bu ada sahip BuildingBlock[`Name`](../../../aspose.words.buildingblocks/buildingblock/name/) içinde mevcut olması gerekir[`GlossaryDocument`](../../../aspose.words/document/glossarydocument/) aksi haldeInvalidOperationException gerçekleşecek.

```csharp
public string PlaceholderName { get; set; }
```

### Örnekler

Yapı taşının içeriğinin, yapılandırılmış bir belge etiketi için özel bir yer tutucu metin olarak nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

// Metin kutusu olarak işlev görecek "PlainText" türünde düz metin yapılandırılmış bir belge etiketi ekleyin.
// Varsayılan olarak göstereceği içerik "Metin girmek için burayı tıklayın" şeklindedir. çabuk.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Etiketin, varsayılan metin yerine bir yapı taşının içeriğini göstermesini sağlayabiliriz.
// İlk olarak, sözlük belgesine içeriği olan bir yapı taşı ekleyin.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;

BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "Custom Placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.AppendChild(new Body(glossaryDoc));
substituteBlock.FirstSection.Body.AppendParagraph("Custom placeholder text.");

glossaryDoc.AppendChild(substituteBlock);

// Ardından, bu yapı taşına ada göre başvuruda bulunmak için yapılandırılmış belge etiketinin "Yer TutucuAdı" özelliğini kullanın.
tag.PlaceholderName = "Custom Placeholder";

// "Yer TutucuAdı", ana belgenin sözlük belgesindeki mevcut bir bloğa atıfta bulunuyorsa,
// "Yer tutucu" özelliği aracılığıyla yapı taşını doğrulayabileceğiz.
Assert.AreEqual(substituteBlock, tag.Placeholder);

// "IsShowingPlaceholderText" özelliğini "true" olarak ayarlayın.
// yapılandırılmış belge etiketinin geçerli içeriği yer tutucu metin olarak.
// Bu, Microsoft Word'deki metin kutusuna tıklandığında, etiketin tüm içeriğinin hemen vurgulanacağı anlamına gelir.
// "IsShowingPlaceholderText" özelliğini "false" olarak ayarlayın.
// içeriğini bir kullanıcının zaten girmiş olduğu metin olarak ele almak için yapılandırılmış belge etiketi.
// Microsoft Word'de bu metne tıklamak, yanıp sönen imleci tıklanan konuma yerleştirecektir.
tag.IsShowingPlaceholderText = isShowingPlaceholderText;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

### Ayrıca bakınız

* class [StructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../structureddocumenttag/)
* toplantı [Aspose.Words](../../../)


