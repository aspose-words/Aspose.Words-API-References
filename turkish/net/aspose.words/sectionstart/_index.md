---
title: SectionStart Enum
linktitle: SectionStart
articleTitle: SectionStart
second_title: .NET için Aspose.Words
description: Bölüm sonlarını anlamak ve daha iyi kontrol ve sunum için belge biçimlendirmesini geliştirmek üzere Aspose.Words.SectionStart enum'unu keşfedin.
type: docs
weight: 6590
url: /tr/net/aspose.words/sectionstart/
---
## SectionStart enumeration

Bölümün başındaki kesme türü.

```csharp
public enum SectionStart
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Continuous | `0` | Yeni bölüm, önceki bölümle aynı sayfada başlar. |
| NewColumn | `1` | Bölüm yeni bir sütundan başlar. |
| NewPage | `2` | Bölüm yeni bir sayfadan başlıyor. |
| EvenPage | `3` | Bölüm yeni bir çift sayfada başlar. |
| OddPage | `4` | Bölüm yeni bir tek sayfadan başlıyor. |

## Örnekler

Aspose.Words belgesinin elle nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Boş bir belge bir bölüm, bir gövde ve bir paragraftan oluşur.
// Tüm bu düğümleri kaldırmak için "RemoveAllChildren" yöntemini çağırın,
// ve çocuğu olmayan bir belge düğümüyle sonuçlanır.
doc.RemoveAllChildren();

// Bu belgenin artık içerik ekleyebileceğimiz bileşik alt düğümleri yok.
// Düzenlemek istersek, düğüm koleksiyonunu yeniden doldurmamız gerekecektir.
// İlk önce yeni bir bölüm oluşturun ve ardından onu kök belge düğümüne bir alt bölüm olarak ekleyin.
Section section = new Section(doc);
doc.AppendChild(section);

// Bölüm için bazı sayfa düzeni özelliklerini ayarlayın.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Bir bölümün, tüm içeriklerini barındıracak ve görüntüleyecek bir gövdeye ihtiyacı vardır
// bölümün üstbilgisi ve altbilgisi arasındaki sayfada.
Body body = new Body(doc);
section.AppendChild(body);

// Bir paragraf oluştur, bazı biçimlendirme özelliklerini ayarla ve sonra onu gövdeye bir alt paragraf olarak ekle.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Son olarak, belgeyi yapmak için biraz içerik ekleyin. Bir çalışma oluşturun,
// Görünümünü ve içeriğini ayarlayın ve ardından paragrafın bir alt öğesi olarak ekleyin.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

Yeni bir bölümün kendisini öncekinden nasıl ayıracağının nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("This text is in section 1.");

// Bölüm sonu türleri, yeni bir bölümün önceki bölümden nasıl ayrılacağını belirler.
// Aşağıda beş tür bölüm sonu bulunmaktadır.
// 1 - Bir sonraki bölümü yeni bir sayfada başlatır:
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("This text is in section 2.");

Assert.AreEqual(SectionStart.NewPage, doc.Sections[1].PageSetup.SectionStart);

// 2 - Mevcut sayfada bir sonraki bölümü başlatır:
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("This text is in section 3.");

Assert.AreEqual(SectionStart.Continuous, doc.Sections[2].PageSetup.SectionStart);

// 3 - Bir sonraki bölümü yeni bir çift sayfada başlatır:
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Writeln("This text is in section 4.");

Assert.AreEqual(SectionStart.EvenPage, doc.Sections[3].PageSetup.SectionStart);

// 4 - Bir sonraki bölümü yeni bir tek sayfada başlatır:
builder.InsertBreak(BreakType.SectionBreakOddPage);
builder.Writeln("This text is in section 5.");

Assert.AreEqual(SectionStart.OddPage, doc.Sections[4].PageSetup.SectionStart);

// 5 - Bir sonraki bölümü yeni bir sütunda başlatır:
TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.SetCount(2);

builder.InsertBreak(BreakType.SectionBreakNewColumn);
builder.Writeln("This text is in section 6.");

Assert.AreEqual(SectionStart.NewColumn, doc.Sections[5].PageSetup.SectionStart);

doc.Save(ArtifactsDir + "PageSetup.SetSectionStart.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
