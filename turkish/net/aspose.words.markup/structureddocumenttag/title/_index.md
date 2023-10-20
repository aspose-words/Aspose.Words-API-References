---
title: StructuredDocumentTag.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words for .NET
description: StructuredDocumentTag Title mülk. Bununla ilişkili kolay adı belirtirSDT . Olamazhükümsüz  C#'da.
type: docs
weight: 290
url: /tr/net/aspose.words.markup/structureddocumenttag/title/
---
## StructuredDocumentTag.Title property

Bununla ilişkili kolay adı belirtir**SDT** . Olamaz`hükümsüz` .

```csharp
public string Title { get; set; }
```

## Örnekler

Düz metin kutusunda yapılandırılmış belge etiketinin nasıl oluşturulacağını ve görünümünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();

// Düz metin içerecek yapılandırılmış bir belge etiketi oluşturun.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Microsoft Word'de yapılandırılmış belge etiketinin üzerine fareyi getirdiğinizde görünen çerçevenin başlığını ve rengini ayarlayın.
tag.Title = "My plain text";
tag.Color = Color.Magenta;

// Bu yapılandırılmış belge etiketi için elde edilebilecek bir etiket ayarlayın
// "tag" adında bir XML öğesi olarak, aşağıdaki dize "@val" özelliğinde.
tag.Tag = "MyPlainTextSDT";

// Her yapılandırılmış belge etiketinin rastgele benzersiz bir kimliği vardır.
Assert.That(tag.Id, Is.Positive);

// Yapılandırılmış belge etiketinin içindeki metnin yazı tipini ayarlayın.
tag.ContentsFont.Name = "Arial";

// Yapılandırılmış belge etiketinin sonundaki metnin yazı tipini ayarlayın.
// Ok tuşlarıyla etiketin dışına çıktıktan sonra belge gövdesine yazdığımız herhangi bir metin bu yazı tipini kullanacaktır.
tag.EndCharacterFont.Name = "Arial Black";

// Varsayılan olarak bu yanlıştır ve yapılandırılmış bir belge etiketinin içindeyken enter tuşuna basmak hiçbir şey yapmaz.
// True olarak ayarlandığında yapılandırılmış belge etiketimiz birden fazla satıra sahip olabilir.

// Yalnızca içeriğe izin vermek için "Multiline" özelliğini "false" olarak ayarlayın
// bu yapılandırılmış belge etiketinin tek bir satıra yayılması.
// Etiketin birden fazla satır içerik içermesine izin vermek için "Multiline" özelliğini "true" olarak ayarlayın.
tag.Multiline = true;

// İçeriğin etrafındaki etiketleri göstermek için "Görünüm" özelliğini "SdtAppearance.Tags" olarak ayarlayın.
 // Varsayılan olarak yapılandırılmış belge etiketi BoundingBox olarak gösterilir.
tag.Appearance = SdtAppearance.Tags;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

// Yapılandırılmış belge etiketimizin bir kopyasını yeni bir paragrafa ekleyin.
StructuredDocumentTag tagClone = (StructuredDocumentTag)tag.Clone(true);
builder.InsertParagraph();
builder.InsertNode(tagClone);

// Yapılandırılmış bir belge etiketini kaldırmak ve içeriğini belgede tutmak için "RemoveSelfOnly" yöntemini kullanın.
tagClone.RemoveSelfOnly();

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlainText.docx");
```

### Ayrıca bakınız

* class [StructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
