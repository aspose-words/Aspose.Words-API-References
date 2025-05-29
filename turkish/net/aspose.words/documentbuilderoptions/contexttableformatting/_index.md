---
title: DocumentBuilderOptions.ContextTableFormatting
linktitle: ContextTableFormatting
articleTitle: ContextTableFormatting
second_title: .NET için Aspose.Words
description: DocumentBuilderOptions'daki ContextTableFormatting özelliğini keşfedin. Tablo biçimlendirmesinin bağımsız kalmasını sağlayarak belgenizin netliğini ve stilini geliştirin.
type: docs
weight: 20
url: /tr/net/aspose.words/documentbuilderoptions/contexttableformatting/
---
## DocumentBuilderOptions.ContextTableFormatting property

Tablo içeriğine uygulanan biçimlendirme, onu izleyen içeriğin biçimlendirmesini etkilemiyorsa doğrudur. Varsayılan değer`doğru` .

```csharp
public bool ContextTableFormatting { get; set; }
```

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

* class [DocumentBuilderOptions](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
