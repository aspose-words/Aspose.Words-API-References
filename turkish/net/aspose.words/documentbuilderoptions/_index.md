---
title: DocumentBuilderOptions Class
linktitle: DocumentBuilderOptions
articleTitle: DocumentBuilderOptions
second_title: .NET için Aspose.Words
description: Kusursuz bir oluşturma deneyimi için özelleştirilebilir özelliklerle belge oluşturmanızı geliştirmek üzere Aspose.Words.DocumentBuilderOptions'ı keşfedin.
type: docs
weight: 670
url: /tr/net/aspose.words/documentbuilderoptions/
---
## DocumentBuilderOptions class

Belge oluşturma süreci için ek seçeneklerin belirtilmesine olanak tanır.

```csharp
public class DocumentBuilderOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [DocumentBuilderOptions](documentbuilderoptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ContextTableFormatting](../../aspose.words/documentbuilderoptions/contexttableformatting/) { get; set; } | Tablo içeriğine uygulanan biçimlendirme, onu izleyen içeriğin biçimlendirmesini etkilemiyorsa doğrudur. Varsayılan değer`doğru` . |
| [DesignMode](../../aspose.words/documentbuilderoptions/designmode/) { get; set; } | Microsoft Word'deki Tasarım Moduna karşılık gelir. |

## Örnekler

İçerik için tablo biçimlendirmesinin nasıl göz ardı edileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Tablodan önce içerik ekler.
// Varsayılan yazı tipi boyutu 12'dir.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Tablo içindeki yazı tipi boyutunu değiştirir.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// ContextTableFormatting true ise, tablo biçimlendirmesi içeriğe uygulanmaz.
// ContextTableFormatting false ise tablo biçimlendirmesi içeriğe sonradan uygulanır.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
