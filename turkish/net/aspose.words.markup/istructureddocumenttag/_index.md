---
title: IStructuredDocumentTag Interface
linktitle: IStructuredDocumentTag
articleTitle: IStructuredDocumentTag
second_title: .NET için Aspose.Words
description: Yapılandırılmış Belge Etiketlerinin etkin yönetimi için Aspose.Words.Markup.IStructuredDocumentTag arayüzünü keşfedin ve bugün belge işleme sürecinizi geliştirin!
type: docs
weight: 4660
url: /tr/net/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface

Ortak bir veri tanımlamak için arayüz[`StructuredDocumentTag`](../structureddocumenttag/) Ve[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/) .

```csharp
public interface IStructuredDocumentTag
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Appearance](../../aspose.words.markup/istructureddocumenttag/appearance/) { get; set; } | Yapılandırılmış belge etiketinin görünümünü alır veya ayarlar. |
| [Color](../../aspose.words.markup/istructureddocumenttag/color/) { get; set; } | Yapılandırılmış belge etiketinin rengini alır veya ayarlar. |
| [Id](../../aspose.words.markup/istructureddocumenttag/id/) { get; } | Bunun için benzersiz, salt okunur, kalıcı bir sayısal Kimlik belirtir**SDT**. |
| [IsMultiSection](../../aspose.words.markup/istructureddocumenttag/ismultisection/) { get; } | Bu örnek aralıklı (çok bölümlü) yapılandırılmış bir belge etiketi ise doğruyu döndürür. |
| [IsShowingPlaceholderText](../../aspose.words.markup/istructureddocumenttag/isshowingplaceholdertext/) { get; set; } | Bu içeriğin ne olduğunu belirtir**SDT** yer tutucu text (SDT içindeki normal metin içeriklerinin aksine) içerecek şekilde yorumlanacaktır. |
| [Level](../../aspose.words.markup/istructureddocumenttag/level/) { get; } | Bu seviyeyi alır**SDT** belge ağacında meydana gelir. |
| [LockContentControl](../../aspose.words.markup/istructureddocumenttag/lockcontentcontrol/) { get; set; } | Bu özellik doğru olarak ayarlandığında, kullanıcının bunu silmesini engelleyecektir**SDT** . |
| [LockContents](../../aspose.words.markup/istructureddocumenttag/lockcontents/) { get; set; } | Bu özellik doğru olarak ayarlandığında, kullanıcının bu içeriği düzenlemesini yasaklayacaktır.**SDT** . |
| [Node](../../aspose.words.markup/istructureddocumenttag/node/) { get; } | Bu arayüzü uygulayan Node nesnesini döndürür. |
| [Placeholder](../../aspose.words.markup/istructureddocumenttag/placeholder/) { get; } | Şunu alır:[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) Bu SDT çalıştırma içeriği boş olduğunda görüntülenmesi gereken yer tutucu metni içeren , belirtilen şekilde ilişkili eşlenen XML öğesi boştur[`XmlMapping`](./xmlmapping/) element veya[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) öğe doğrudur. |
| [PlaceholderName](../../aspose.words.markup/istructureddocumenttag/placeholdername/) { get; set; } | Adını alır veya ayarlar[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) yer tutucu metin içeren. |
| [SdtType](../../aspose.words.markup/istructureddocumenttag/sdttype/) { get; } | Bunun türünü alır**Yapılandırılmış belge etiketi** . |
| [Tag](../../aspose.words.markup/istructureddocumenttag/tag/) { get; set; } | Geçerli SDT düğümüyle ilişkili bir etiketi belirtir. Boş olamaz. |
| [Title](../../aspose.words.markup/istructureddocumenttag/title/) { get; set; } | Bu ile ilişkili dostça adı belirtir**SDT** . Boş olamaz. |
| [WordOpenXML](../../aspose.words.markup/istructureddocumenttag/wordopenxml/) { get; } | Düğümün içinde bulunan XML'i temsil eden bir dize alırFlatOpc biçim. |
| [XmlMapping](../../aspose.words.markup/istructureddocumenttag/xmlmapping/) { get; } | Bu yapılandırılmış belge etiketinin geçerli belgenin özel bir XML bölümündeki XML data eşlemesini temsil eden bir nesne alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetChildNodes](../../aspose.words.markup/istructureddocumenttag/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Belirtilen türlerle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [RemoveSelfOnly](../../aspose.words.markup/istructureddocumenttag/removeselfonly/)() | Yalnızca bu SDT düğümünü kaldırır, ancak içeriğini belge ağacının içinde tutar. |

## Örnekler

Yapılandırılmış belge etiketinin nasıl kaldırılacağını gösterir, ancak içeriği içeride tutar.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

 // Bu koleksiyon, aralıklı ve aralıksız yapılandırılmış etiketlere erişim için birleşik bir arayüz sağlar.
IEnumerable<IStructuredDocumentTag> sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(5, sdts.Count());

// Burada, aralıklı ve aralıksız yapılandırılmış etiketlerin ortak arayüzünden alt düğümleri alabiliriz.
foreach (IStructuredDocumentTag sdt in sdts)
    if (sdt.GetChildNodes(NodeType.Any, false).Count > 0)
        sdt.RemoveSelfOnly();

sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(0, sdts.Count());
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)
