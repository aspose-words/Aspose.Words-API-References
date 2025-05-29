---
title: StoryType Enum
linktitle: StoryType
articleTitle: StoryType
second_title: .NET için Aspose.Words
description: Aspose.Words.StoryType enum'u keşfedin, Word belge metin hikayelerini kolaylıkla ve verimli bir şekilde yönetin. Belge işleme deneyiminizi bugün geliştirin!
type: docs
weight: 6970
url: /tr/net/aspose.words/storytype/
---
## StoryType enumeration

Word belgesinin metni hikayelerde saklanır.`StoryType` bir hikayeyi tanımlar.

```csharp
public enum StoryType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Varsayılan değer. Belgede böyle bir hikaye yok. |
| MainText | `1` | Belgenin ana metnini içerir ve şu şekilde gösterilir:[`Body`](../body/) . |
| Footnotes | `2` | Dipnot metnini içerir ve şu şekilde gösterilir:[`Footnote`](../../aspose.words.notes/footnote/) . |
| Endnotes | `3` | Dipnot metnini içerir, şu şekilde gösterilir:[`Footnote`](../../aspose.words.notes/footnote/) . |
| Comments | `4` | Belge yorumlarını (açıklamaları) içerir ve şunlarla temsil edilir:[`Comment`](../comment/) . |
| Textbox | `5` | Şekil veya metin kutusu metnini içerir ve şu şekilde gösterilir:[`Shape`](../../aspose.words.drawing/shape/) . |
| EvenPagesHeader | `6` | Çift sayfaların üstbilgisinin metnini içerir ve şu şekilde gösterilir:[`HeaderFooter`](../headerfooter/) . |
| PrimaryHeader | `7` | Birincil başlığın metnini içerir. Başlık tek ve çift sayfalar için farklı olduğunda, tek sayfaların başlığının metnini içerir. Tarafından temsil edilir[`HeaderFooter`](../headerfooter/) . |
| EvenPagesFooter | `8` | Çift sayfaların altbilgisinin metnini içerir, şu şekilde gösterilir:[`HeaderFooter`](../headerfooter/) . |
| PrimaryFooter | `9` | Birincil altbilginin metnini içerir. Altbilgi tek ve çift sayfalar için farklı olduğunda, tek sayfaların altbilgisinin metnini içerir. Tarafından temsil edilir[`HeaderFooter`](../headerfooter/) . |
| FirstPageHeader | `10` | İlk sayfa başlığının metnini içerir ve şu şekilde gösterilir:[`HeaderFooter`](../headerfooter/) . |
| FirstPageFooter | `11` | İlk sayfa altbilgisinin metnini içerir ve şu şekilde gösterilir:[`HeaderFooter`](../headerfooter/) . |
| FootnoteSeparator | `12` | Dipnot ayırıcısının metnini içerir. |
| FootnoteContinuationSeparator | `13` | Dipnot devam ayırıcısının metnini içerir. |
| FootnoteContinuationNotice | `14` | Dipnot devam bildirimi ayırıcısının metnini içerir. |
| EndnoteSeparator | `15` | Dipnot ayırıcısının metnini içerir. |
| EndnoteContinuationSeparator | `16` | Dipnot devam ayırıcısının metnini içerir. |
| EndnoteContinuationNotice | `17` | Dipnot devam bildirimi ayırıcısının metnini içerir. |

## Örnekler

Bir düğümden tüm şekillerin nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir şekil eklemek için bir DocumentBuilder kullanın. Bu bir satır içi şekildir,
// ilk bölümün Gövdesinin bir alt düğümü olan bir ana Paragrafı vardır.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Bu Gövdenin alt paragraflarından tüm şekilleri silebiliriz.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
