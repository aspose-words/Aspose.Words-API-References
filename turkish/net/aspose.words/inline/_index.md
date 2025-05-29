---
title: Inline Class
linktitle: Inline
articleTitle: Inline
second_title: .NET için Aspose.Words
description: Satır içi düğümlerde karakter biçimlendirmesi için tasarlanmış Aspose.Words.Inline sınıfını keşfedin. Alt düğümler olmadan belgenizin stilini geliştirin!
type: docs
weight: 3710
url: /tr/net/aspose.words/inline/
---
## Inline class

Karakter biçimlendirmesiyle ilişkilendirilebilen ancak kendi alt düğümlerine sahip olamayan satır içi düzey düğümler için temel sınıf.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Bir Belgedeki Düğümlerin Mantıksal Düzeyleri](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/) belgeleme makalesi.

```csharp
public abstract class Inline : Node
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [Font](../../aspose.words/inline/font/) { get; } | Bu nesnenin yazı tipi biçimlendirmesine erişim sağlar. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Geri Döndürür`doğru` eğer bu düğüm diğer düğümleri içerebiliyorsa. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Değişiklik izleme etkinleştirilmişken bu nesnenin Microsoft Word'de silinmesi durumunda doğru değerini döndürür. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Değişiklik izleme etkinleştirilmişken Microsoft Word'de nesnenin biçimlendirmesinin değiştirilmesi durumunda doğru değerini döndürür. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Bu nesnenin Microsoft Word'e değişiklik izleme etkinleştirilmişken eklenip eklenmediğini döndürür. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Geri Döndürür`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinleştirilmişken taşınırsa (silinirse). |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Geri Döndürür`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinleştirilmişken taşınırsa (eklenirse). |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümü hemen takip eden düğümü alır. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Bu düğümün türünü alır. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün en yakın üst düğümünü alır. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Üst öğeyi alır[`Paragraph`](../paragraph/) bu düğümün. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir[`Range`](../range/)bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Bir ziyaretçiyi kabul eder. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Belirtilenin ilk atasını alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atasını alır. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ön sipariş ağacı geçiş algoritmasına göre bir sonraki düğümü alır. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini ana öğeden kaldırır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

## Notlar

Bir sınıftan türetilmiş`Inline` bir çocuğu olabilir[`Paragraph`](../paragraph/).

## Örnekler

Satır içi bir düğümün revizyon türünün nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// İnceleme -> İzleme'de bulunan "Değişiklikleri İzle" seçeneğiyle belgeyi düzenlediğimizde,
// Microsoft Word'de açık olduğunda uyguladığımız değişiklikler revizyon olarak sayılır.
// Aspose.Words kullanarak bir belgeyi düzenlerken, revizyonları şu şekilde izlemeye başlayabiliriz:
// belgenin "StartTrackRevisions" metodunu çağırarak ve "StopTrackRevisions" metodunu kullanarak izlemeyi durdurarak.
// Revizyonları belgeye entegre etmek için kabul edebiliriz
// veya önerilen değişikliği etkili bir şekilde değiştirmek için bunları reddedin.
Assert.AreEqual(6, doc.Revisions.Count);

// Bir revizyonun üst düğümü, revizyonun ilgilendiği çalıştırmadır. Bir Çalıştırma, bir Satır İçi düğümdür.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// Aşağıda, bir Inline düğümünü işaretleyebilecek beş tür revizyon bulunmaktadır.
// 1 - Bir "ekle" revizyon:
// Bu revizyon, değişiklikleri izlerken metin eklediğimizde gerçekleşir.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - Bir "format" revizyonu:
// Bu revizyon, değişiklikleri izlerken metnin biçimlendirmesini değiştirdiğimizde gerçekleşir.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - "Taşınma" revizyonundan:
// Microsoft Word'de metni vurguladığımızda ve ardından onu belgede farklı bir yere sürüklediğimizde
// Değişiklikleri izlerken iki revizyon görünüyor.
// "Taşıma" revizyonunun kopyası, taşımadan önce metnin orijinal halinin bir kopyasıdır.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - "Taşınacak" revizyon:
// "Taşı" revizyon, belgedeki yeni konumuna taşıdığımız metindir.
// Gerçekleştirdiğimiz her taşıma revizyonu için "Şuradan taşı" ve "Şuraya taşı" revizyonları çiftler halinde görünür.
// Bir taşıma revizyonunu kabul etmek, "taşınacak" revizyonunu ve metnini siler,
// ve "taşınacak" revizyondaki metni tutar.
// Bir taşıma revizyonunu reddetmek ise tam tersine "taşınacak yer" revizyonunu korur ve "taşınacak yer" revizyonunu siler.
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - Bir "silme" revizyonu:
// Bu revizyon, değişiklikleri izlerken metni sildiğimizde meydana gelir. Metni bu şekilde sildiğimizde,
// revizyonu kabul edene kadar belgede bir revizyon olarak kalacaktır,
// ya metni tamamen silecek ya da revizyonu reddedecek, bu da sildiğimiz metni olduğu yerde tutacak.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Ayrıca bakınız

* class [Node](../node/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
