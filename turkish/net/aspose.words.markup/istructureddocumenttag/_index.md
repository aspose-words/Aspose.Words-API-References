---
title: Interface IStructuredDocumentTag
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Markup.IStructuredDocumentTag arayüz. Ortak bir veri tanımlamak için arayüzStructuredDocumentTag VeStructuredDocumentTagRangeStart .
type: docs
weight: 3970
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
| [Color](../../aspose.words.markup/istructureddocumenttag/color/) { get; set; } | Yapılandırılmış belge etiketinin rengini alır veya ayarlar. |
| [Id](../../aspose.words.markup/istructureddocumenttag/id/) { get; } | Bunun için benzersiz bir salt okunur kalıcı sayısal kimlik belirtir **SDT**. |
| [IsShowingPlaceholderText](../../aspose.words.markup/istructureddocumenttag/isshowingplaceholdertext/) { get; set; } | Bunun içeriğinin olup olmadığını belirtir. **SDT** metin yer tutucusunu içerecek şekilde yorumlanacaktır (SDT içindeki normal metin içeriklerinin aksine). |
| [Level](../../aspose.words.markup/istructureddocumenttag/level/) { get; } | Bunun hangi düzeyde olduğunu alır **SDT** belge ağacında oluşur. |
| [LockContentControl](../../aspose.words.markup/istructureddocumenttag/lockcontentcontrol/) { get; set; } | Doğru olarak ayarlandığında bu özellik kullanıcının bunu silmesini yasaklar **SDT** . |
| [LockContents](../../aspose.words.markup/istructureddocumenttag/lockcontents/) { get; set; } | Doğru olarak ayarlandığında bu özellik, kullanıcının bu içeriği düzenlemesini yasaklar **SDT** . |
| [Placeholder](../../aspose.words.markup/istructureddocumenttag/placeholder/) { get; } | Alır[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)Bu SDT çalıştırma içerikleri boş olduğunda görüntülenmesi gereken yer tutucu metni içeren, ilişkili eşlenen XML öğesi,[`XmlMapping`](./xmlmapping/) element veya[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) unsur doğrudur. |
| [PlaceholderName](../../aspose.words.markup/istructureddocumenttag/placeholdername/) { get; set; } | Adını alır veya ayarlar[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) yer tutucu metni içerir. |
| [SdtType](../../aspose.words.markup/istructureddocumenttag/sdttype/) { get; } | Bunun türünü alır **Yapılandırılmış belge etiketi** . |
| [Tag](../../aspose.words.markup/istructureddocumenttag/tag/) { get; set; } | Geçerli SDT düğümüyle ilişkili bir etiketi belirtir. Boş olamaz. |
| [Title](../../aspose.words.markup/istructureddocumenttag/title/) { get; set; } | Bununla ilişkili kolay adı belirtir **SDT** . Boş olamaz. |
| [WordOpenXML](../../aspose.words.markup/istructureddocumenttag/wordopenxml/) { get; } | Düğümdeki düğümün içerdiği XML'i temsil eden bir dize alır.FlatOpc format. |
| [XmlMapping](../../aspose.words.markup/istructureddocumenttag/xmlmapping/) { get; } | Bu yapılandırılmış belge etiketinin, geçerli belgenin özel bir XML bölümündeki XML data ile eşlenmesini temsil eden bir nesne alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [IsRanged](../../aspose.words.markup/istructureddocumenttag/isranged/)() | Bu örneğin aralıklı yapılandırılmış bir belge etiketi olması durumunda true değerini döndürür. |
| [StructuredDocumentTagNode](../../aspose.words.markup/istructureddocumenttag/structureddocumenttagnode/)() | Bu arayüzü uygulayan Düğüm nesnesini döndürür. |

### Ayrıca bakınız

* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)


