---
title: Run
second_title: Aspose.Words for .NET API Referansı
description: Yeni bir örneğini başlatır Koşmak sınıf.
type: docs
weight: 10
url: /tr/net/aspose.words/run/run/
---
## Run(DocumentBase) {#constructor}

Yeni bir örneğini başlatır **Koşmak** sınıf.

```csharp
public Run(DocumentBase doc)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | DocumentBase | Sahip belgesi. |

### Notlar

Ne zaman **Koşmak** oluşturulur, belirtilen belgeye aittir, ancak henüz belgenin bir parçası değil ve **Üst Düğüm** boş.

Eklemek **Koşmak** belgeye, çalıştırmanın eklenmesini istediğiniz paragrafta InsertAfter veya InsertBefore kullanın.

### Örnekler

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

### Ayrıca bakınız

* class [DocumentBase](../../documentbase)
* class [Run](../../run)
* ad alanı [Aspose.Words](../../run)
* toplantı [Aspose.Words](../../../)

---

## Run(DocumentBase, string) {#constructor_1}

Yeni bir örneğini başlatır **Koşmak** sınıf.

```csharp
public Run(DocumentBase doc, string text)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | DocumentBase | Sahip belgesi. |
| text | String | Koşunun metni. |

### Notlar

Ne zaman **Koşmak** oluşturulur, belirtilen belgeye aittir, ancak henüz belgenin bir parçası değil ve **Üst Düğüm** boş.

Eklemek **Koşmak** belgeye, çalıştırmanın eklenmesini istediğiniz paragrafta InsertAfter veya InsertBefore kullanın.

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

### Ayrıca bakınız

* class [DocumentBase](../../documentbase)
* class [Run](../../run)
* ad alanı [Aspose.Words](../../run)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->