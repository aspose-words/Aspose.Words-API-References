---
title: Inline Class
linktitle: Inline
articleTitle: Inline
second_title: Aspose.Words for .NET
description: Aspose.Words.Inline sınıf. Kendileriyle ilişkilendirilmiş karakter biçimlendirmesine sahip olabilen ancak kendilerine ait alt düğümlere sahip olamayan satır içi düzey düğümler için temel sınıf C#'da.
type: docs
weight: 3260
url: /tr/net/aspose.words/inline/
---
## Inline class

Kendileriyle ilişkilendirilmiş karakter biçimlendirmesine sahip olabilen ancak kendilerine ait alt düğümlere sahip olamayan satır içi düzey düğümler için temel sınıf.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Bir Belgedeki Düğümlerin Mantıksal Düzeyleri](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/) dokümantasyon makalesi.

```csharp
public abstract class Inline : Node
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [Font](../../aspose.words/inline/font/) { get; } | Bu nesnenin yazı tipi formatlamasına erişim sağlar. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | İadeler`doğru` bu düğüm başka düğümler içeriyorsa. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Değişiklik izleme etkinken bu nesne Microsoft Word'de silinmişse true değerini döndürür. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Microsoft Word'de değişiklik izleme etkinken nesnenin biçimlendirmesi değiştirilmişse doğru değerini döndürür. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Bu nesne Microsoft Word'e değişiklik izleme etkinken eklenmişse doğru değerini döndürür. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | İadeler`doğru` değişiklik izleme etkinken bu nesne Microsoft Word'de taşındıysa (silindiyse). |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | İadeler`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinken taşınmışsa (eklenmişse). |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonra gelen düğümü alır. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Bu düğümün türünü alır. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün doğrudan ebeveynini alır. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Üst öğeyi alır[`Paragraph`](../paragraph/) bu düğümün. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir değeri döndürür[`Range`](../range/) Bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Ziyaretçi kabul eder. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Belirtilenin ilk atayı alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atayı alır. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ön sipariş ağaç geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Düğümün içeriğini belirtilen formatta bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

## Notlar

Türetilmiş bir sınıf`Inline` çocuğu olabilir[`Paragraph`](../paragraph/).

## Örnekler

Satır içi düğümün revizyon türünün nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// Belgeyi düzenlediğimizde, Gözden Geçirme yoluyla bulunan "Değişiklikleri İzle" seçeneği -> Takip,
// Microsoft Word'de açıldığında uyguladığımız değişiklikler revizyon olarak sayılır.
// Aspose.Words kullanarak bir belgeyi düzenlerken, revizyonları izlemeye şu şekilde başlayabiliriz:
// belgenin "StartTrackRevisions" yöntemini çağırıyoruz ve "StopTrackRevisions" yöntemini kullanarak izlemeyi durduruyoruz.
// Belgeye asimile etmek için düzeltmeleri kabul edebiliriz
// veya önerilen değişikliği etkili bir şekilde değiştirmek için onları reddedin.
Assert.AreEqual(6, doc.Revisions.Count);

// Bir revizyonun ana düğümü, revizyonun ilgili olduğu çalıştırmadır. Çalıştırma bir Satır İçi düğümdür.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// Aşağıda bir Satır İçi düğümü işaretleyebilen beş tür revizyon bulunmaktadır.
// 1 - Bir "ekleme" revizyonu:
// Bu revizyon, değişiklikleri takip ederken metin eklediğimizde meydana gelir.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - Bir "format" revizyonu:
// Bu revizyon, değişiklikleri takip ederken metnin formatını değiştirdiğimizde ortaya çıkar.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - Bir "şuradan taşıma" revizyonu:
// Microsoft Word'de metni vurgulayıp belgede farklı bir yere sürüklediğimizde
// Değişiklikleri takip ederken iki revizyon belirir.
// "Şuradan taşı" revizyonu, metnin biz taşımadan önceki orijinal kopyasıdır.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - Bir "geçiş" revizyonu:
// "Taşı" revizyonu, belgedeki yeni konumuna taşıdığımız metindir.
// Gerçekleştirdiğimiz her hareket revizyonu için "Şuraya Taşı" ve "Şuraya Taşı" revizyonları çift olarak görünür.
// Bir taşıma revizyonunu kabul etmek, "şuradan taşıma" revizyonunu ve metnini siler,
// ve metni "şuraya taşı" revizyonundan korur.
// Bir taşıma revizyonunu reddetmek, tam tersine, "şuraya taşı" revizyonunu korur ve "şuraya taşı" revizyonunu siler.
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - Bir "silme" revizyonu:
// Değişiklikleri takip ederken metni sildiğimizde bu revizyon meydana gelir. Bunun gibi bir metni sildiğimizde,
// biz revizyonu kabul edene kadar belgede revizyon olarak kalacak,
// bu, metni tamamen silecek veya revizyonu reddedecek, bu da sildiğimiz metni olduğu yerde tutacak.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Ayrıca bakınız

* class [Node](../node/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
