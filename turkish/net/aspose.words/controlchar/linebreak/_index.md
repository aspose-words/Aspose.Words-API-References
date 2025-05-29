---
title: ControlChar.LineBreak
linktitle: LineBreak
articleTitle: LineBreak
second_title: .NET için Aspose.Words
description: x000b veya v karakteriyle kusursuz metin biçimlendirme için ControlChar LineBreak alanını keşfedin. İçeriğinizin okunabilirliğini bugün artırın!
type: docs
weight: 120
url: /tr/net/aspose.words/controlchar/linebreak/
---
## ControlChar.LineBreak field

Satır sonu karakteri: "\x000b" veya "\v".

```csharp
public static readonly string LineBreak;
```

## Örnekler

Bir belgeye çeşitli kontrol karakterlerinin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Normal bir boşluk ekle.
builder.Write("Before space." + ControlChar.SpaceChar + "After space.");

// Bölünemez bir boşluk olan NBSP ekleyin.
// Normal boşluktan farklı olarak, bu boşluğun bulunduğu konumda otomatik satır sonu olamaz.
builder.Write("Before space." + ControlChar.NonBreakingSpace + "After space.");

// Bir sekme karakteri ekle.
builder.Write("Before tab." + ControlChar.Tab + "After tab.");

// Satır sonu ekle.
builder.Write("Before line break." + ControlChar.LineBreak + "After line break.");

// Yeni bir satır ekler ve yeni bir paragraf başlatır.
Assert.AreEqual(1, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);
builder.Write("Before line feed." + ControlChar.LineFeed + "After line feed.");
Assert.AreEqual(2, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// Satır besleme karakterinin iki versiyonu vardır.
Assert.AreEqual(ControlChar.LineFeed, ControlChar.Lf);

// Satır sonları ve satır beslemeleri birlikte tek bir karakterle temsil edilebilir.
Assert.AreEqual(ControlChar.CrLf, ControlChar.Cr + ControlChar.Lf);

// Yeni bir paragraf başlatacak bir paragraf sonu ekleyin.
builder.Write("Before paragraph break." + ControlChar.ParagraphBreak + "After paragraph break.");
Assert.AreEqual(3, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// Bölüm sonu ekle. Bu yeni bir bölüm veya paragraf oluşturmaz.
Assert.AreEqual(1, doc.Sections.Count);
builder.Write("Before section break." + ControlChar.SectionBreak + "After section break.");
Assert.AreEqual(1, doc.Sections.Count);

// Sayfa sonu ekle.
builder.Write("Before page break." + ControlChar.PageBreak + "After page break.");

// Sayfa sonu, bölüm sonu ile aynı değere sahiptir.
Assert.AreEqual(ControlChar.PageBreak, ControlChar.SectionBreak);

// Yeni bir bölüm ekleyin ve ardından sütun sayısını ikiye ayarlayın.
doc.AppendChild(new Section(doc));
builder.MoveToSection(1);
builder.CurrentSection.PageSetup.TextColumns.SetCount(2);

// Metnin bir sonraki sütuna geçeceği noktayı işaretlemek için bir kontrol karakteri kullanabiliriz.
builder.Write("Text at end of column 1." + ControlChar.ColumnBreak + "Text at beginning of column 2.");

doc.Save(ArtifactsDir + "ControlChar.InsertControlChars.docx");

// Çoğu karakterin char ve string karşılıkları vardır.
Assert.AreEqual(Convert.ToChar(ControlChar.Cell), ControlChar.CellChar);
Assert.AreEqual(Convert.ToChar(ControlChar.NonBreakingSpace), ControlChar.NonBreakingSpaceChar);
Assert.AreEqual(Convert.ToChar(ControlChar.Tab), ControlChar.TabChar);
Assert.AreEqual(Convert.ToChar(ControlChar.LineBreak), ControlChar.LineBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.LineFeed), ControlChar.LineFeedChar);
Assert.AreEqual(Convert.ToChar(ControlChar.ParagraphBreak), ControlChar.ParagraphBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.SectionBreak), ControlChar.SectionBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.PageBreak), ControlChar.SectionBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.ColumnBreak), ControlChar.ColumnBreakChar);
```

### Ayrıca bakınız

* class [ControlChar](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
