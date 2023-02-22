---
title: Class Run
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Run sınıf. Aynı yazı tipi biçimlendirmesine sahip bir dizi karakteri temsil eder.
type: docs
weight: 4560
url: /tr/net/aspose.words/run/
---
## Run class

Aynı yazı tipi biçimlendirmesine sahip bir dizi karakteri temsil eder.

```csharp
public class Run : Inline
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Run](run/#constructor)(DocumentBase) | Yeni bir örneğini başlatır **Koşmak** sınıf. |
| [Run](run/#constructor_1)(DocumentBase, string) | Yeni bir örneğini başlatır **Koşmak** sınıf. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [Font](../../aspose.words/inline/font/) { get; } | Bu nesnenin yazı tipi biçimlendirmesine erişim sağlar. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Bu düğüm başka düğümler içerebiliyorsa true değerini döndürür. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Bu nesne, değişiklik izleme etkinleştirilirken Microsoft Word'de silindiyse true değerini döndürür. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Değişiklik izleme etkinken nesnenin biçimlendirmesi Microsoft Word'de değiştirilirse doğru döndürür. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Bu nesne, değişiklik izleme etkinken Microsoft Word'e eklendiyse true değerini döndürür. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | İade **doğru** değişiklik izleme etkinken bu nesne Microsoft Word'de taşındıysa (silindiyse). |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | İade **doğru** bu nesne, değişiklik izleme etkinken Microsoft Word'de taşındıysa (yerleştirildiyse). |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| override [NodeType](../../aspose.words/run/nodetype/) { get; } | İade **DüğümTürü.Çalıştır** . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün hemen üst öğesini alır. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Üst öğeyi alır[`Paragraph`](../paragraph/) bu düğümün. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |
| [Text](../../aspose.words/run/text/) { get; set; } | Çalıştırmanın metnini alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words/run/accept/)(DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Belirtilenin ilk atasını alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Belirtilen nesne türünün ilk üst öğesini alır. |
| override [GetText](../../aspose.words/run/gettext/)() | Çalıştırmanın metnini alır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

### Notlar

Belgenin tüm metni, metin dizilerinde saklanır.

**Koşmak** sadece çocuğu olabilir **Paragraf** veya satır içi **YapılandırılmışBelge Etiketi**.

### Örnekler

Font özelliğini kullanarak bir metin akışının nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

Bir Aspose.Words belgesinin elle nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Boş bir belge bir bölüm, bir gövde ve bir paragraf içerir.
// Tüm bu düğümleri kaldırmak için "RemoveAllChildren" yöntemini çağırın,
// ve alt öğesi olmayan bir belge düğümüyle bitirin.
doc.RemoveAllChildren();

// Bu belgede artık içerik ekleyebileceğimiz bileşik alt düğüm yok.
// Düzenlemek istiyorsak, düğüm koleksiyonunu yeniden doldurmamız gerekecek.
// Önce yeni bir bölüm oluşturun ve ardından onu kök belge düğümüne alt öğe olarak ekleyin.
Section section = new Section(doc);
doc.AppendChild(section);

// Bölüm için bazı sayfa kurulum özelliklerini ayarlayın.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Bir bölümün tüm içeriğini içerecek ve görüntüleyecek bir gövdeye ihtiyacı var
// bölümün üstbilgisi ve altbilgisi arasındaki sayfada.
Body body = new Body(doc);
section.AppendChild(body);

// Bir paragraf oluşturun, bazı biçimlendirme özelliklerini ayarlayın ve ardından onu alt öğe olarak gövdeye ekleyin.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Son olarak, belgeyi yapmak için biraz içerik ekleyin. Bir koşu oluşturun,
// görünümünü ve içeriğini ayarlayın ve ardından paragrafa alt öğe olarak ekleyin.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

Bir CompositeNode'un alt öğeleri koleksiyonunda alt düğümlerin nasıl ekleneceğini, güncelleneceğini ve silineceğini gösterir.

```csharp
Document doc = new Document();

// Varsayılan olarak boş bir belgenin bir paragrafı vardır.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Paragrafımız gibi bileşik düğümler, alt öğe olarak diğer bileşik ve satır içi düğümleri içerebilir.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Üç çalıştırma düğümü daha oluşturun.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Belge gövdesi, biz bunları bir bileşik düğüme ekleyene kadar bu çalıştırmaları görüntülemeyecektir.
// bu, ilk çalıştırmada yaptığımız gibi, belgenin düğüm ağacının bir parçasıdır.
// Eklediğimiz düğümlerin metin içeriklerinin nerede olduğunu belirleyebiliriz
// paragraftaki başka bir düğüme göre bir ekleme konumu belirterek belgede görünür.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// İkinci çalıştırmayı ilk çalıştırmanın önündeki paragrafa ekleyin.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// İlk çalıştırmadan sonra üçüncü çalıştırmayı ekleyin.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// İlk çalıştırmayı paragrafın alt düğüm koleksiyonunun başına ekleyin.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Mevcut alt düğümleri düzenleyip silerek çalıştırmanın içeriğini değiştirebiliriz.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Ayrıca bakınız

* class [Inline](../inline/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


