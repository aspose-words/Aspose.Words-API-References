---
title: StoryType Enum
linktitle: StoryType
articleTitle: StoryType
second_title: Aspose.Words for .NET
description: Aspose.Words.StoryType Sıralama. Bir Word belgesinin metni hikayelerde saklanır.StoryType bir hikayeyi tanımlar C#'da.
type: docs
weight: 6120
url: /tr/net/aspose.words/storytype/
---
## StoryType enumeration

Bir Word belgesinin metni hikayelerde saklanır.`StoryType` bir hikayeyi tanımlar.

```csharp
public enum StoryType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Varsayılan değer. Belgede böyle bir hikaye yok. |
| MainText | `1` | Belgenin şu şekilde temsil edilen ana metnini içerir:[`Body`](../body/) . |
| Footnotes | `2` | Aşağıdakilerle temsil edilen dipnot metnini içerir:[`Footnote`](../../aspose.words.notes/footnote/) . |
| Endnotes | `3` | Aşağıdakilerle temsil edilen son not metnini içerir:[`Footnote`](../../aspose.words.notes/footnote/) . |
| Comments | `4` | Şununla temsil edilen belge yorumlarını (ek açıklamalar) içerir:[`Comment`](../comment/) . |
| Textbox | `5` | Şekli veya metin kutusu metnini içerir; şu şekilde temsil edilir:[`Shape`](../../aspose.words.drawing/shape/) . |
| EvenPagesHeader | `6` | Çift sayfalar başlığının metnini içerir; şu şekilde temsil edilir:[`HeaderFooter`](../headerfooter/) . |
| PrimaryHeader | `7` | Birincil başlığın metnini içerir. Başlık tek ve çift sayfalar için farklı olduğunda, tek sayfalar başlığının metnini içerir. İle temsil edilen[`HeaderFooter`](../headerfooter/) . |
| EvenPagesFooter | `8` | Çift sayfalar altbilgisinin metnini içerir; şu şekilde temsil edilir:[`HeaderFooter`](../headerfooter/) . |
| PrimaryFooter | `9` | Birincil altbilginin metnini içerir. Altbilgi tek ve çift sayfalar için farklı olduğunda, tek sayfaların altbilgisinin metnini içerir. İle temsil edilen[`HeaderFooter`](../headerfooter/) . |
| FirstPageHeader | `10` | İlk sayfa başlığının metnini içerir; şu şekilde temsil edilir:[`HeaderFooter`](../headerfooter/) . |
| FirstPageFooter | `11` | İlk sayfa altbilgisinin metnini içerir; şu şekilde temsil edilir:[`HeaderFooter`](../headerfooter/) . |
| FootnoteSeparator | `12` | Dipnot ayırıcının metnini içerir; şu şekilde temsil edilir:FootnoteSeparator . |
| FootnoteContinuationSeparator | `13` | Dipnot devam ayırıcısının metnini içerir; şu şekilde temsil edilir:FootnoteSeparator . |
| FootnoteContinuationNotice | `14` | Dipnot devamı bildirim ayırıcısının metnini içerir; şu şekilde temsil edilir:FootnoteSeparator . |
| EndnoteSeparator | `15` | Son not ayırıcının metnini içerir; şu şekilde temsil edilir:FootnoteSeparator . |
| EndnoteContinuationSeparator | `16` | Son not devam ayırıcısının metnini içerir; şu şekilde temsil edilir:FootnoteSeparator . |
| EndnoteContinuationNotice | `17` | Son not devam bildirimi ayırıcısının metnini içerir; şu şekilde temsil edilir:FootnoteSeparator . |

## Örnekler

Bir düğümdeki tüm şekillerin nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Şekil eklemek için DocumentBuilder'ı kullanın. Bu satır içi bir şekildir,
// birinci bölümün Gövdesinin alt düğümü olan bir ana Paragrafa sahiptir.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Bu Gövdenin alt paragraflarındaki tüm şekilleri silebiliriz.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
