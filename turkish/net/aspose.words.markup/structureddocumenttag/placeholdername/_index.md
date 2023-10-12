---
title: StructuredDocumentTag.PlaceholderName
second_title: Aspose.Words for .NET API Referansı
description: StructuredDocumentTag mülk. Adını alır veya ayarlarBuildingBlock yer tutucu metni içerir.
type: docs
weight: 240
url: /tr/net/aspose.words.markup/structureddocumenttag/placeholdername/
---
## StructuredDocumentTag.PlaceholderName property

Adını alır veya ayarlar[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/) yer tutucu metni içerir.

[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/) bu isimle[`Name`](../../../aspose.words.buildingblocks/buildingblock/name/) içinde mevcut olması gerekir[`GlossaryDocument`](../../../aspose.words/document/glossarydocument/) aksi takdirdeInvalidOperationException gerçekleşecek.

```csharp
public string PlaceholderName { get; set; }
```

### Örnekler

Bir yapı taşının içeriğinin, yapılandırılmış bir belge etiketi için özel yer tutucu metin olarak nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

// Metin kutusu işlevi görecek "Düz Metin" türünde düz metin yapılı bir belge etiketi ekleyin.
// Varsayılan olarak görüntüleyeceği içerik "Metin girmek için burayı tıklayın." çabuk.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Etiketin, varsayılan metin yerine bir yapı taşının içeriğini görüntülemesini sağlayabiliriz.
// Öncelikle sözlük belgesine içeriği olan bir yapı taşı ekleyin.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;

BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "Custom Placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.AppendChild(new Body(glossaryDoc));
substituteBlock.FirstSection.Body.AppendParagraph("Custom placeholder text.");

glossaryDoc.AppendChild(substituteBlock);

// Daha sonra, o yapı bloğuna ada göre başvuruda bulunmak için yapılandırılmış belge etiketinin "PlaceholderName" özelliğini kullanın.
tag.PlaceholderName = "Custom Placeholder";

// "Yer TutucuAdı" ana belgenin sözlük belgesindeki mevcut bir bloğa atıfta bulunuyorsa,
// "Placeholder" özelliği aracılığıyla yapı bloğunu doğrulayabileceğiz.
Assert.AreEqual(substituteBlock, tag.Placeholder);

// "IsShowingPlaceholderText" özelliğini "true" olarak ayarlayarak
// yapılandırılmış belge etiketinin mevcut içeriği yer tutucu metin olarak.
// Bu, Microsoft Word'deki metin kutusuna tıklandığında etiketin tüm içeriğinin hemen vurgulanacağı anlamına gelir.
// "IsShowingPlaceholderText" özelliğini "false" olarak ayarlayarak
// içeriğini kullanıcının önceden girdiği metin olarak ele alacak yapılandırılmış belge etiketi.
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


