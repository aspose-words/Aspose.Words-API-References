---
title: ControlChar Class
linktitle: ControlChar
articleTitle: ControlChar
second_title: .NET için Aspose.Words
description: Belgelerinizdeki kontrol karakterlerini etkili bir şekilde yönetmek, biçimlendirmeyi ve okunabilirliği artırmak için Aspose.Words.ControlChar sınıfını keşfedin.
type: docs
weight: 550
url: /tr/net/aspose.words/controlchar/
---
## ControlChar class

Belgelerde sıklıkla karşılaşılan kontrol karakterleri.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Kontrol Karakterleriyle Çalışma](https://docs.aspose.com/words/net/working-with-control-characters/) belgeleme makalesi.

```csharp
public static class ControlChar
```

## Alanlar

| İsim | Tanım |
| --- | --- |
| static readonly [Cell](../../aspose.words/controlchar/cell/) | Bir tablo hücresinin sonu veya bir tablo satırının sonu karakteri: "\x0007" veya "\a". |
| const [CellChar](../../aspose.words/controlchar/cellchar/) | Bir tablo hücresinin sonu veya bir tablo satırının sonu karakteri: (char)7 veya "\a". |
| static readonly [ColumnBreak](../../aspose.words/controlchar/columnbreak/) | Sütun sonu karakteri: "\x000e". |
| const [ColumnBreakChar](../../aspose.words/controlchar/columnbreakchar/) | Sütun sonu karakteri: (char)14. |
| static readonly [Cr](../../aspose.words/controlchar/cr/) | Satır başı karakteri: "\x000d" veya "\r". Aynı[`ParagraphBreak`](./paragraphbreak/) . |
| static readonly [CrLf](../../aspose.words/controlchar/crlf/) | Satır başı ve ardından satır besleme karakteri: "\x000d\x000a" veya "\r\n". Microsoft Word belgelerinde olduğu gibi kullanılmaz, ancak metin dosyalarında paragraf sonları için yaygın olarak kullanılır. |
| const [DefaultTextInputChar](../../aspose.words/controlchar/defaulttextinputchar/) | Bu, metin girişi form alanlarında varsayılan değer olarak kullanılan "o" karakteridir. |
| const [FieldEndChar](../../aspose.words/controlchar/fieldendchar/) | MS Word alan karakterinin sonu: (char)21. |
| const [FieldSeparatorChar](../../aspose.words/controlchar/fieldseparatorchar/) | Alan ayırıcı karakteri, alan kodunu alan değerinden ayırır. Bazı alanlarda isteğe bağlıdır. Değer: (char)20. |
| const [FieldStartChar](../../aspose.words/controlchar/fieldstartchar/) | MS Word alan karakterinin başlangıcı: (char)19. |
| static readonly [Lf](../../aspose.words/controlchar/lf/) | Satır besleme karakteri: "\x000a" veya "\n". Aynı[`LineFeed`](./linefeed/) . |
| static readonly [LineBreak](../../aspose.words/controlchar/linebreak/) | Satır sonu karakteri: "\x000b" veya "\v". |
| const [LineBreakChar](../../aspose.words/controlchar/linebreakchar/) | Satır sonu karakteri: (char)11 veya "\v". |
| static readonly [LineFeed](../../aspose.words/controlchar/linefeed/) | Satır besleme karakteri: "\x000a" veya "\n". Aynı[`Lf`](./lf/) . |
| const [LineFeedChar](../../aspose.words/controlchar/linefeedchar/) | Satır besleme karakteri: (char)10 veya "\n". |
| const [NonBreakingHyphenChar](../../aspose.words/controlchar/nonbreakinghyphenchar/) | Microsoft Word'de Kesintisiz Tire (char)30'dur. |
| static readonly [NonBreakingSpace](../../aspose.words/controlchar/nonbreakingspace/) | Bölünemez boşluk karakteri: "\x00a0". |
| const [NonBreakingSpaceChar](../../aspose.words/controlchar/nonbreakingspacechar/) | Bölünmez boşluk karakteri: (char)160. |
| const [OptionalHyphenChar](../../aspose.words/controlchar/optionalhyphenchar/) | Microsoft Word'de İsteğe Bağlı Tire (char)31'dir. |
| static readonly [PageBreak](../../aspose.words/controlchar/pagebreak/) | Sayfa sonu karakteri: "\x000c" veya "\f". Aynı değere sahip olduğunu unutmayın[`SectionBreak`](./sectionbreak/) . |
| const [PageBreakChar](../../aspose.words/controlchar/pagebreakchar/) | Sayfa sonu karakteri: (char)12 veya "\f". |
| static readonly [ParagraphBreak](../../aspose.words/controlchar/paragraphbreak/) | Paragraf sonu karakteri: "\x000d" veya "\r". Aynı[`Cr`](./cr/) |
| const [ParagraphBreakChar](../../aspose.words/controlchar/paragraphbreakchar/) | Paragraf sonu karakteri: (char)13 veya "\r". |
| static readonly [SectionBreak](../../aspose.words/controlchar/sectionbreak/) | Bölüm sonu karakteri: "\x000c" veya "\f". Aynı değere sahip olduğunu unutmayın[`PageBreak`](./pagebreak/) . |
| const [SectionBreakChar](../../aspose.words/controlchar/sectionbreakchar/) | Bölüm sonu karakteri: (char)12 veya "\f". |
| const [SpaceChar](../../aspose.words/controlchar/spacechar/) | Boşluk karakteri: (char)32. |
| static readonly [Tab](../../aspose.words/controlchar/tab/) | Sekme karakteri: "\x0009" veya "\t". |
| const [TabChar](../../aspose.words/controlchar/tabchar/) | Sekme karakteri: (char)9 veya "\t". |

## Notlar

Aynı sabitlerin hem char hem de string versiyonlarını sağlar. Örneğin: string[`LineBreak`](./linebreak/) ve karakter[`LineBreakChar`](./linebreakchar/) aynı değere sahip.

## Örnekler

Kontrol karakterlerinin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// DocumentBuilder ile metin içeren paragraflar ekleyin.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Belgenin metin biçimine dönüştürülmesi, kontrol karakterlerinin ortaya çıkmasını sağlar
// sayfa sonları gibi belgenin bazı yapısal öğelerini temsil eder.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// Bir belgeyi dize biçimine dönüştürürken,
// Trim metoduyla bazı kontrol karakterlerini atlayabiliriz.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
