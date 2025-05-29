---
title: StructuredDocumentTag.PlaceholderName
linktitle: PlaceholderName
articleTitle: PlaceholderName
second_title: .NET için Aspose.Words
description: BuildingBlock adlarını kolayca yönetmek ve belgenizin yer tutucu metnini geliştirmek için StructuredDocumentTag PlaceholderName özelliğini keşfedin.
type: docs
weight: 240
url: /tr/net/aspose.words.markup/structureddocumenttag/placeholdername/
---
## StructuredDocumentTag.PlaceholderName property

Adını alır veya ayarlar[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/) yer tutucu metin içeren.

```csharp
public string PlaceholderName { get; set; }
```

### istisnalar

| istisna | şart |
| --- | --- |
| InvalidOperationException | Bu isimde bir BuildingBlock atın[`Name`](../../../aspose.words.buildingblocks/buildingblock/name/) içinde mevcut değil[`GlossaryDocument`](../../../aspose.words/document/glossarydocument/). |

## Örnekler

Yapı bloğunun içeriğinin yapılandırılmış bir belge etiketi için özel yer tutucu metin olarak nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

// "PlainText" türünde, metin kutusu işlevi görecek düz metin yapılandırılmış bir belge etiketi ekleyin.
// Varsayılan olarak gösterilecek içerik "Metin girmek için buraya tıklayın." istemidir.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Varsayılan metin yerine yapı bloğunun içeriğini görüntülemek için etiketi alabiliriz.
// Öncelikle sözlük belgesine içerikli bir yapı taşı ekleyelim.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;

BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "Custom Placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.AppendChild(new Body(glossaryDoc));
substituteBlock.FirstSection.Body.AppendParagraph("Custom placeholder text.");

glossaryDoc.AppendChild(substituteBlock);

// Ardından, bu yapı bloğuna adıyla başvurmak için yapılandırılmış belge etiketinin "PlaceholderName" özelliğini kullanın.
tag.PlaceholderName = "Custom Placeholder";

// "PlaceholderName" ana belgenin sözlük belgesindeki mevcut bir bloğa atıfta bulunuyorsa,
// "Yer Tutucu" özelliği aracılığıyla yapı bloğunu doğrulayabileceğiz.
Assert.AreEqual(substituteBlock, tag.Placeholder);

// "IsShowingPlaceholderText" özelliğini "true" olarak ayarlayın.
// yapılandırılmış belge etiketinin geçerli içeriği yer tutucu metin olarak.
// Bu, Microsoft Word'deki metin kutusuna tıklandığında etiketin tüm içeriğinin hemen vurgulanacağı anlamına gelir.
// "IsShowingPlaceholderText" özelliğini "false" olarak ayarlayın ve
// İçeriğini kullanıcının daha önce girdiği metin olarak ele alan yapılandırılmış belge etiketi.
// Microsoft Word'de bu metne tıklandığında yanıp sönen imleç tıklanan yere yerleşecektir.
tag.IsShowingPlaceholderText = isShowingPlaceholderText;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

### Ayrıca bakınız

* class [StructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
