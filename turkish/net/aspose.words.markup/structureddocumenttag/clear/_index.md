---
title: StructuredDocumentTag.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words for .NET
description: StructuredDocumentTag Clear yöntem. Bu yapılandırılmış belge etiketinin içeriğini temizler ve tanımlanmışsa bir yer tutucu görüntüler C#'da.
type: docs
weight: 340
url: /tr/net/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag.Clear method

Bu yapılandırılmış belge etiketinin içeriğini temizler ve tanımlanmışsa bir yer tutucu görüntüler.

```csharp
public void Clear()
```

## Notlar

Yapılandırılmış belge etiketinin revizyonları varsa içeriğinin temizlenmesi mümkün değildir.

Bu yapılandırılmış belge etiketi özel XML ile eşlenirse (kullanılarak[`XmlMapping`](../xmlmapping/) özelliği), başvurulan XML düğümü temizlenir.

## Örnekler

Yapılandırılmış belge etiketi öğelerinin içeriğinin nasıl silineceğini gösterir.

```csharp
Document doc = new Document();

// Düz metin yapılı bir belge etiketi oluşturun ve ardından bunu belgeye ekleyin.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Metin kutusu biçimindeki bu yapılandırılmış belge etiketi zaten yer tutucu metni görüntüler.
Assert.AreEqual("Click here to enter text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// Metin içerikli bir yapı taşı oluşturun.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;
BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "My placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.EnsureMinimum();
substituteBlock.FirstSection.Body.FirstParagraph.AppendChild(new Run(glossaryDoc, "Custom placeholder text."));
glossaryDoc.AppendChild(substituteBlock);

// Yapılandırılmış belge etiketinin "PlaceholderName" özelliğini yapı taşımızın adına ayarlayın.
// orijinal varsayılan metnin yerine yapı taşının içeriğini görüntülemek için yapılandırılmış belge etiketi.
tag.PlaceholderName = "My placeholder";

Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// Yapılandırılmış belge etiketinin metnini düzenleyin ve yer tutucu metni gizleyin.
Run run = (Run)tag.GetChild(NodeType.Run, 0, true);
run.Text = "New text.";
tag.IsShowingPlaceholderText = false;

Assert.AreEqual("New text.", tag.GetText().Trim());

// Bu yapılandırılmış belge etiketinin içeriğini temizlemek ve yer tutucuyu yeniden görüntülemek için "Temizle" yöntemini kullanın.
tag.Clear();

Assert.True(tag.IsShowingPlaceholderText);
Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
```

### Ayrıca bakınız

* class [StructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
