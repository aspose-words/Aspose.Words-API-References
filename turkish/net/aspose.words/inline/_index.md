---
title: Inline
second_title: Aspose.Words for .NET API Referansı
description: Kendileriyle ilişkilendirilmiş karakter biçimlendirmesine sahip olabilen ancak kendi alt düğümlerine sahip olamayan satır içi düzey düğümler için temel sınıf.
type: docs
weight: 3060
url: /tr/net/aspose.words/inline/
---
## Inline class

Kendileriyle ilişkilendirilmiş karakter biçimlendirmesine sahip olabilen, ancak kendi alt düğümlerine sahip olamayan satır içi düzey düğümler için temel sınıf.

```csharp
public abstract class Inline : Node
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [Font](../../aspose.words/inline/font) { get; } | Bu nesnenin yazı tipi biçimlendirmesine erişim sağlar. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Bu düğüm başka düğümler içerebiliyorsa true değerini döndürür. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision) { get; } | Bu nesne, değişiklik izleme etkinleştirilirken Microsoft Word'de silindiyse true değerini döndürür. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision) { get; } | Değişiklik izleme etkinken nesnenin biçimlendirmesi Microsoft Word'de değiştirilirse doğru döndürür. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision) { get; } | Bu nesne, değişiklik izleme etkinken Microsoft Word'e eklendiyse true değerini döndürür. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision) { get; } | İade **doğru** değişiklik izleme etkinken bu nesne Microsoft Word'de taşındıysa (silindiyse). |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision) { get; } | İade **doğru** bu nesne, değişiklik izleme etkinken Microsoft Word'de taşındıysa (yerleştirildiyse). |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| abstract [NodeType](../../aspose.words/node/nodetype) { get; } | Bu düğümün türünü alır. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Bu düğümün hemen üst öğesini alır. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph) { get; } | Üst öğeyi alır[`Paragraph`](../paragraph) bu düğümün. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept)(DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [Clone](../../aspose.words/node/clone)(bool) | Düğümün bir kopyasını oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Belirtilenin ilk atasını alır[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Belirtilen nesne türünün ilk üst öğesini alır. |
| virtual [GetText](../../aspose.words/node/gettext)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove)() | Kendini üst öğeden kaldırır. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

### Notlar

türetilmiş bir sınıf **Çizgide** çocuğu olabilir **Paragraf**.

### Örnekler

Bir satır içi düğümün revizyon türünün nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// Belgeyi düzenlediğimizde "Değişiklikleri İzle" seçeneği, İnceleme -> izleme,
// Microsoft Word'de açık, uyguladığımız değişiklikler revizyon olarak sayılır.
// Aspose.Words kullanarak bir belgeyi düzenlerken, revizyonları şu şekilde izlemeye başlayabiliriz:
// belgenin "StartTrackRevisions" yöntemini çağırarak ve "StopTrackRevisions" yöntemini kullanarak izlemeyi durdurun.
// Revizyonları belgeye asimile etmek için kabul edebiliriz
// veya önerilen değişikliği etkili bir şekilde değiştirmek için onları reddedin.
Assert.AreEqual(6, doc.Revisions.Count);

// Bir revizyonun üst düğümü, revizyonun ilgili olduğu çalıştırmadır. Bir Çalıştırma, bir Satır içi düğümdür.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// Aşağıda, bir Satır içi düğümü işaretleyebilen beş tür revizyon bulunmaktadır.
// 1 - Bir "insert" revizyonu:
// Bu revizyon, değişiklikleri takip ederken metin eklediğimizde gerçekleşir.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - Bir "biçim" revizyonu:
// Bu revizyon, değişiklikleri takip ederken metnin formatını değiştirdiğimizde gerçekleşir.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - Bir "geçiş" revizyonu:
// Microsoft Word'de metni vurgulayıp belgede farklı bir yere sürüklediğimizde
// değişiklikleri takip ederken iki revizyon görünür.
// "Move from" revizyonu, metnin biz onu taşımadan önceki orijinal kopyasıdır.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - "Taşı" revizyonu:
// "Taşı" revizyonu, belgedeki yeni konumuna taşıdığımız metindir.
// Yaptığımız her hareket revizyonu için "Move from" ve "move to" revizyonları çiftler halinde görünür.
// Bir taşıma revizyonunu kabul etmek, "move from" revizyonunu ve metnini siler,
// ve metni "move to" revizyonundan tutar.
// Bir taşıma revizyonunu reddetmek, tersine, "move from" revizyonunu korur ve "move to" revizyonunu siler.
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - Bir "sil" revizyonu:
// Bu revizyon, değişiklikleri takip ederken metni sildiğimizde gerçekleşir. Böyle bir metni sildiğimizde,
// biz revizyonu kabul edene kadar belgede revizyon olarak kalacak,
// metni tamamen silecek veya düzeltmeyi reddedecek, bu da sildiğimiz metni olduğu yerde tutacak.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Ayrıca bakınız

* class [Node](../node)
* ad alanı [Aspose.Words](../../aspose.words)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
