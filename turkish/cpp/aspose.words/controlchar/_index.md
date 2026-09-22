---
title: "Aspose::Words::ControlChar class"
linktitle: "ControlChar"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ControlChar sınıfı. Kontrol karakterleri belgelerde sıkça karşılaşılır. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 18000
url: /tr/cpp/aspose.words/controlchar/
---
## ControlChar class


Belgelerde sıkça karşılaşılan kontrol karakterleri. Daha fazla bilgi edinmek için [Working With Control Characters](https://docs.aspose.com/words/cpp/working-with-control-characters/) dokümantasyon makalesini ziyaret edin.

```cpp
class ControlChar
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| static [Cell](./cell/)() | Bir tablo hücresinin sonu veya bir tablo satırının sonu karakteri: "\x0007" veya "\a". |
| static [ColumnBreak](./columnbreak/)() | Sütun sonu karakteri: "\x000e". |
| [ControlChar](./controlchar/)() |  |
| static [Cr](./cr/)() | Satır başı karakteri: "\x000d" veya "\r". Aynı [ParagraphBreak](./paragraphbreak/) ile. |
| static [CrLf](./crlf/)() | Satır başı ardından satır beslemesi karakteri: "\x000d\x000a" veya "\r\n". Microsoft Word belgelerinde bu şekilde kullanılmaz, ancak paragraf sonları için metin dosyalarında yaygın olarak kullanılır. |
| static [Lf](./lf/)() | Satır beslemesi karakteri: "\x000a" veya "\n". Aynı [LineFeed](./linefeed/) ile. |
| static [LineBreak](./linebreak/)() | Satır sonu karakteri: "\x000b" veya "\v". |
| static [LineFeed](./linefeed/)() | Satır beslemesi karakteri: "\x000a" veya "\n". Aynı [Lf](./lf/) ile. |
| static [NonBreakingSpace](./nonbreakingspace/)() | Bölünemez boşluk karakteri: "\x00a0". |
| static [PageBreak](./pagebreak/)() | Sayfa sonu karakteri: "\x000c" veya "\f". Not: aynı değere [SectionBreak](./sectionbreak/) sahiptir. |
| static [ParagraphBreak](./paragraphbreak/)() | Paragraf sonu karakteri: "\x000d" veya "\r". Aynı [Cr](./cr/) ile |
| static [SectionBreak](./sectionbreak/)() | Bölüm sonu karakteri: "\x000c" veya "\f". Not: aynı değere [PageBreak](./pagebreak/) sahiptir. |
| static [Tab](./tab/)() | Sekme karakteri: "\x0009" veya "\t". |
## Alanlar

| Alan | Açıklama |
| --- | --- |
| static constexpr [CellChar](./cellchar/) | Bir tablo hücresinin sonu veya bir tablo satırının sonu karakteri: (char)7 veya "\a". |
| static constexpr [ColumnBreakChar](./columnbreakchar/) | Sütun sonu karakteri: (char)14. |
| static constexpr [DefaultTextInputChar](./defaulttextinputchar/) | Bu, metin girişi form alanlarında varsayılan değer olarak kullanılan "o" karakteridir. |
| static constexpr [FieldEndChar](./fieldendchar/) | MS Word alanının sonu karakteri: (char)21. |
| static constexpr [FieldSeparatorChar](./fieldseparatorchar/) | Alan ayırıcı karakter, alan kodunu alan değerinden ayırır. Bazı alanlarda isteğe bağlıdır. Değer: (char)20. |
| static constexpr [FieldStartChar](./fieldstartchar/) | MS Word alanının başlangıç karakteri: (char)19. |
| static constexpr [LineBreakChar](./linebreakchar/) | Satır sonu karakteri: (char)11 veya "\v". |
| static constexpr [LineFeedChar](./linefeedchar/) | Satır besleme karakteri: (char)10 veya "\n". |
| static constexpr [NonBreakingHyphenChar](./nonbreakinghyphenchar/) | Microsoft Word'te kesintisiz tire (char)30'dur. |
| static constexpr [NonBreakingSpaceChar](./nonbreakingspacechar/) | Kesintisiz boşluk karakteri: (char)160. |
| static constexpr [OptionalHyphenChar](./optionalhyphenchar/) | Microsoft Word'te isteğe bağlı tire (char)31'dir. |
| static constexpr [PageBreakChar](./pagebreakchar/) | Sayfa sonu karakteri: (char)12 veya "\f". |
| static constexpr [ParagraphBreakChar](./paragraphbreakchar/) | Paragraf sonu karakteri: (char)13 veya "\r". |
| static constexpr [SectionBreakChar](./sectionbreakchar/) | Bölüm sonu karakteri: (char)12 veya "\f". |
| static constexpr [SpaceChar](./spacechar/) | Boşluk karakteri: (char)32. |
| static constexpr [TabChar](./tabchar/) | Sekme karakteri: (char)9 veya "\t". |

## Örnekler



Kontrol karakterlerinin nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// DocumentBuilder ile metin içeren paragraflar ekleyin.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Belgeyi metin biçimine dönüştürmek, kontrol karakterlerinin
// belgenin bazı yapısal öğelerini, örneğin sayfa sonlarını, temsil eder.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + System::String::Format(u"Hello again!{0}", Aspose::Words::ControlChar::Cr()) + Aspose::Words::ControlChar::PageBreak(), doc->GetText());

// Bir belgeyi dize biçimine dönüştürürken,
// Trim yöntemiyle bazı kontrol karakterlerini atlayabiliriz.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
