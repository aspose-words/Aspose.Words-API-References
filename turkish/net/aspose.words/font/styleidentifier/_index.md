---
title: Font.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words for .NET
description: Font StyleIdentifier mülk. Bu biçimlendirmeye uygulanan karakter stilinin yerel ayardan bağımsız stil tanımlayıcısını alır veya ayarlar C#'da.
type: docs
weight: 410
url: /tr/net/aspose.words/font/styleidentifier/
---
## Font.StyleIdentifier property

Bu biçimlendirmeye uygulanan karakter stilinin yerel ayardan bağımsız stil tanımlayıcısını alır veya ayarlar.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

## Örnekler

Mevcut metnin stilinin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda stillere referans vermenin iki yolu verilmiştir.
// 1 - Stil adının kullanılması:
builder.Font.StyleName = "Emphasis";
builder.Writeln("Text originally in \"Emphasis\" style");

// 2 - Yerleşik bir stil tanımlayıcı kullanma:
builder.Font.StyleIdentifier = StyleIdentifier.IntenseEmphasis;
builder.Writeln("Text originally in \"Intense Emphasis\" style");

// Bir stilin tüm kullanımlarını diğerine dönüştürün,
// eski ve yeni stillere referans vermek için yukarıdaki yöntemleri kullanıyoruz.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true).OfType<Run>())
{
    if (run.Font.StyleName == "Emphasis")
        run.Font.StyleName = "Strong";

    if (run.Font.StyleIdentifier == StyleIdentifier.IntenseEmphasis)
        run.Font.StyleIdentifier = StyleIdentifier.Strong;
}

doc.Save(ArtifactsDir + "Font.ChangeStyle.docx");
```

### Ayrıca bakınız

* enum [StyleIdentifier](../../styleidentifier/)
* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
