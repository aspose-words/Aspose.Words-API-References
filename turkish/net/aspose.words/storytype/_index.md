---
title: Enum StoryType
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.StoryType Sıralama. Bir Word belgesinin metni hikayelerde saklanır. Öykü Türü bir hikayeyi tanımlar.
type: docs
weight: 5820
url: /tr/net/aspose.words/storytype/
---
## StoryType enumeration

Bir Word belgesinin metni hikayelerde saklanır. **Öykü Türü** bir hikayeyi tanımlar.

```csharp
public enum StoryType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Varsayılan değer. Belgede böyle bir hikaye yok. |
| MainText | `1` | ile temsil edilen belgenin ana metnini içerir.[`Body`](../body/) . |
| Footnotes | `2` | ile temsil edilen dipnot metnini içerir[`Footnote`](../../aspose.words.notes/footnote/) . |
| Endnotes | `3` | İle temsil edilen son not metnini içerir[`Footnote`](../../aspose.words.notes/footnote/) . |
| Comments | `4` | ile temsil edilen belge yorumlarını (açıklamaları) içerir.[`Comment`](../comment/) . |
| Textbox | `5` | İle temsil edilen şekil veya metin kutusu metnini içerir[`Shape`](../../aspose.words.drawing/shape/) . |
| EvenPagesHeader | `6` | ile temsil edilen çift sayfalar başlığının metnini içerir[`HeaderFooter`](../headerfooter/) . |
| PrimaryHeader | `7` | Birincil başlığın metnini içerir. Tek ve çift sayfalar için başlık farklı olduğunda, tek sayfalar başlığının metnini içerir. İle temsil edilen[`HeaderFooter`](../headerfooter/) . |
| EvenPagesFooter | `8` | ile temsil edilen çift sayfa altbilgisinin metnini içerir[`HeaderFooter`](../headerfooter/) . |
| PrimaryFooter | `9` | Birincil altbilginin metnini içerir. Tek ve çift sayfalar için altbilgi farklı olduğunda, tek sayfa altbilgisinin metnini içerir. İle temsil edilen[`HeaderFooter`](../headerfooter/) . |
| FirstPageHeader | `10` | ile temsil edilen ilk sayfa başlığının metnini içerir[`HeaderFooter`](../headerfooter/) . |
| FirstPageFooter | `11` | İle temsil edilen ilk sayfa altbilgisinin metnini içerir[`HeaderFooter`](../headerfooter/) . |
| FootnoteSeparator | `12` | ile temsil edilen dipnot ayırıcı metnini içerirFootnoteSeparator . |
| FootnoteContinuationSeparator | `13` | ile temsil edilen dipnot devam ayırıcısının metnini içerirFootnoteSeparator . |
| FootnoteContinuationNotice | `14` | ile temsil edilen dipnot devam bildirimi ayırıcısının metnini içerirFootnoteSeparator . |
| EndnoteSeparator | `15` | İle temsil edilen son not ayırıcı metnini içerirFootnoteSeparator . |
| EndnoteContinuationSeparator | `16` | ile temsil edilen son not devam ayırıcısının metnini içerirFootnoteSeparator . |
| EndnoteContinuationNotice | `17` | ile temsil edilen son not devam bildirimi ayırıcısının metnini içerirFootnoteSeparator . |

### Örnekler

Bir düğümden tüm şekillerin nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Şekil eklemek için DocumentBuilder kullanın. Bu bir satır içi şekil,
// birinci bölümün Gövdesinin alt düğümü olan bir üst Paragrafı olan.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Bu Body'nin alt paragraflarından tüm şekilleri silebiliriz.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


