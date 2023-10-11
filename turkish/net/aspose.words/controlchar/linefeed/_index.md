---
title: ControlChar.LineFeed
second_title: Aspose.Words for .NET API Referansı
description: ControlChar alan. Satır besleme karakteri x000a veya n. İle aynıLf .
type: docs
weight: 140
url: /tr/net/aspose.words/controlchar/linefeed/
---
## ControlChar.LineFeed field

Satır besleme karakteri: "\x000a" veya "\n". İle aynı[`Lf`](../lf/) .

```csharp
public static readonly string LineFeed;
```

### Örnekler

Bir belgeye çeşitli kontrol karakterlerinin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Normal bir boşluk ekleyin.
builder.Write("Before space." + ControlChar.SpaceChar + "After space.");

// Bölünemeyen bir alan olan bir NBSP ekleyin.
// Normal alanın aksine, bu alanın konumunda otomatik satır sonu bulunamaz.
builder.Write("Before space." + ControlChar.NonBreakingSpace + "After space.");

// Bir sekme karakteri ekleyin.
builder.Write("Before tab." + ControlChar.Tab + "After tab.");

// Satır sonu ekleyin.
builder.Write("Before line break." + ControlChar.LineBreak + "After line break.");

// Yeni bir satır ekleyin ve yeni bir paragraf başlatın.
Assert.AreEqual(1, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);
builder.Write("Before line feed." + ControlChar.LineFeed + "After line feed.");
Assert.AreEqual(2, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// Satır besleme karakterinin iki versiyonu vardır.
Assert.AreEqual(ControlChar.LineFeed, ControlChar.Lf);

// Satırbaşları ve satır beslemeleri bir karakterle birlikte temsil edilebilir.
Assert.AreEqual(ControlChar.CrLf, ControlChar.Cr + ControlChar.Lf);

// Yeni bir paragraf başlatacak bir paragraf sonu ekleyin.
builder.Write("Before paragraph break." + ControlChar.ParagraphBreak + "After paragraph break.");
Assert.AreEqual(3, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// Bölüm sonu ekleyin. Bu yeni bir bölüm veya paragraf oluşturmaz.
Assert.AreEqual(1, doc.Sections.Count);
builder.Write("Before section break." + ControlChar.SectionBreak + "After section break.");
Assert.AreEqual(1, doc.Sections.Count);

//Sayfa sonu ekleyin.
builder.Write("Before page break." + ControlChar.PageBreak + "After page break.");

// Sayfa sonu, bölüm sonuyla aynı değerdedir.
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
* ad alanı [Aspose.Words](../../controlchar/)
* toplantı [Aspose.Words](../../../)


