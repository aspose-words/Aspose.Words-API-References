---
title: Font.StyleName
linktitle: StyleName
articleTitle: StyleName
second_title: .NET için Aspose.Words
description: Font StyleName özelliğini keşfedin, projelerinizde gelişmiş metin biçimlendirme ve tasarım esnekliği için karakter stillerini kolayca yönetin.
type: docs
weight: 430
url: /tr/net/aspose.words/font/stylename/
---
## Font.StyleName property

Bu biçimlendirmeye uygulanan karakter stilinin adını alır veya ayarlar.

```csharp
public string StyleName { get; set; }
```

## Örnekler

Mevcut metnin stilinin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda stillere referans vermenin iki yolu bulunmaktadır.
// 1 - Stil adını kullanarak:
builder.Font.StyleName = "Emphasis";
builder.Writeln("Text originally in \"Emphasis\" style");

// 2 - Yerleşik bir stil tanımlayıcısı kullanarak:
builder.Font.StyleIdentifier = StyleIdentifier.IntenseEmphasis;
builder.Writeln("Text originally in \"Intense Emphasis\" style");

// Bir stilin tüm kullanımlarını diğerine dönüştür,
// yukarıdaki yöntemleri kullanarak eski ve yeni stillere referans vermek.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true))
{
    if (run.Font.StyleName == "Emphasis")
        run.Font.StyleName = "Strong";

    if (run.Font.StyleIdentifier == StyleIdentifier.IntenseEmphasis)
        run.Font.StyleIdentifier = StyleIdentifier.Strong;
}

doc.Save(ArtifactsDir + "Font.ChangeStyle.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
