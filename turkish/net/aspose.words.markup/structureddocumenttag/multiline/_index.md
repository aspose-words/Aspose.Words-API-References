---
title: StructuredDocumentTag.Multiline
linktitle: Multiline
articleTitle: Multiline
second_title: .NET için Aspose.Words
description: Gelişmiş belge esnekliği ve kullanıcı deneyimi için birden fazla satır metin kullanılmasını sağlayan StructuredDocumentTag Çok Satırlı özelliğini keşfedin.
type: docs
weight: 210
url: /tr/net/aspose.words.markup/structureddocumenttag/multiline/
---
## StructuredDocumentTag.Multiline property

Bunun olup olmadığını belirtir**SDT** birden fazla satır metne izin verir.

```csharp
public bool Multiline { get; set; }
```

## Notlar

Bu özelliğe erişim yalnızca şu amaçlar için çalışacaktır:RichText VePlainText SDT türü.

Diğer tüm SDT tipleri için istisna oluşacaktır.

## Örnekler

Düz metin kutusunda yapılandırılmış bir belge etiketinin nasıl oluşturulacağını ve görünümünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();

// Düz metin içerecek yapılandırılmış bir belge etiketi oluşturun.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Microsoft Word'de yapılandırılmış belge etiketinin üzerine geldiğinizde görünen çerçevenin başlığını ve rengini ayarlayın.
tag.Title = "My plain text";
tag.Color = Color.Magenta;

// Bu yapılandırılmış belge etiketi için elde edilebilir bir etiket ayarlayın
// "etiket" adında bir XML öğesi olarak, "@val" özniteliğinde aşağıdaki dize ile.
tag.Tag = "MyPlainTextSDT";

// Her yapılandırılmış belge etiketinin rastgele ve benzersiz bir kimliği vardır.
Assert.IsTrue(tag.Id > 0);

// Yapılandırılmış belge etiketi içindeki metnin yazı tipini ayarlayın.
tag.ContentsFont.Name = "Arial";

// Yapılandırılmış belge etiketinin sonundaki metnin yazı tipini ayarlayın.
// Etiketten ok tuşlarıyla çıktıktan sonra belge gövdesine yazdığımız her metin bu fontu kullanacaktır.
tag.EndCharacterFont.Name = "Arial Black";

// Varsayılan olarak bu yanlıştır ve yapılandırılmış bir belge etiketi içindeyken enter'a basmak hiçbir şey yapmaz.
// True olarak ayarlandığında, yapılandırılmış belge etiketimiz birden fazla satıra sahip olabilir.

// Yalnızca içeriklere izin vermek için "Çok satırlı" özelliğini "false" olarak ayarlayın
// Bu yapılandırılmış belge etiketinin tek bir satıra yayılması.
// Etiketin birden fazla satır içerik içermesine izin vermek için "Çok Satırlı" özelliğini "true" olarak ayarlayın.
tag.Multiline = true;

// İçeriğin etrafındaki etiketleri göstermek için "Görünüm" özelliğini "SdtAppearance.Tags" olarak ayarlayın.
 // Varsayılan olarak yapılandırılmış belge etiketi BoundingBox olarak gösterilir.
tag.Appearance = SdtAppearance.Tags;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

// Yapılandırılmış belge etiketimizin bir klonunu yeni bir paragrafa ekleyin.
StructuredDocumentTag tagClone = (StructuredDocumentTag)tag.Clone(true);
builder.InsertParagraph();
builder.InsertNode(tagClone);

// İçeriğini belgede tutarak yapılandırılmış bir belge etiketini kaldırmak için "RemoveSelfOnly" yöntemini kullanın.
tagClone.RemoveSelfOnly();

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlainText.docx");
```

### Ayrıca bakınız

* class [StructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
