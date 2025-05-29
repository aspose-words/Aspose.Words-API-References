---
title: ReplacerContext Class
linktitle: ReplacerContext
articleTitle: ReplacerContext
second_title: .NET için Aspose.Words
description: Sorunsuz bul ve değiştir işlemleri için Aspose.Words LowCode ReplacerContext sınıfını keşfedin, belge otomasyonunuzu ve verimliliğinizi artırın.
type: docs
weight: 4350
url: /tr/net/aspose.words.lowcode/replacercontext/
---
## ReplacerContext class

Bul/değiştir işlemi bağlamı.

```csharp
public class ReplacerContext : ProcessorContext
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [ReplacerContext](replacercontext/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [FindReplaceOptions](../../aspose.words.lowcode/replacercontext/findreplaceoptions/) { get; } | Bul/değiştir seçenekleri. |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | İşlemci tarafından kullanılan yazı tipi ayarları. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | İşlemci tarafından kullanılan belge düzeni seçenekleri. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | İşlemci tarafından kullanılan uyarı geri araması. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [SetReplacement](../../aspose.words.lowcode/replacercontext/setreplacement/#setreplacement_1)(*Regex, string*) | Bul/değiştir işlemi tarafından kullanılan deseni ve değiştirmeyi ayarlar. |
| [SetReplacement](../../aspose.words.lowcode/replacercontext/setreplacement/#setreplacement)(*string, string*) | Bul/değiştir işlemi tarafından kullanılan deseni ve değiştirmeyi ayarlar. |

## Örnekler

Belgedeki dizenin, bağlam kullanılarak regex ile nasıl değiştirileceğini gösterir.

```csharp
// Belgede string ifadeleri regex ile değiştirmenin birkaç yolu vardır:
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

ReplacerContext replacerContext = new ReplacerContext();
replacerContext.SetReplacement(pattern, replacement);
replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

Replacer.Create(replacerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.ReplaceContextRegex.docx")
    .Execute();
```

Belgedeki dizenin bağlam kullanılarak nasıl değiştirileceğini gösterir.

```csharp
// Belgedeki dizeleri değiştirmenin birkaç yolu vardır:
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

ReplacerContext replacerContext = new ReplacerContext();
replacerContext.SetReplacement(pattern, replacement);
replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

Replacer.Create(replacerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.ReplaceContext.docx")
    .Execute();
```

Bağlam kullanılarak akıştaki belgeler kullanılarak belgedeki dizenin nasıl değiştirileceğini gösterir.

```csharp
// Akıştaki belgeleri kullanarak belgedeki dizeyi değiştirmenin birkaç yolu vardır:
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

using (FileStream streamIn = new FileStream(MyDir + "Footer.docx", FileMode.Open, FileAccess.Read))
{
    ReplacerContext replacerContext = new ReplacerContext();
    replacerContext.SetReplacement(pattern, replacement);
    replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceContextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Create(replacerContext)
        .From(streamIn)
        .To(streamOut, SaveFormat.Docx)
        .Execute();
}
```

Bağlam kullanılarak akıştan alınan belgelerde dizenin regex ile nasıl değiştirileceğini gösterir.

```csharp
// Akıştaki belgeleri kullanarak belgedeki dizeyi regex ile değiştirmenin birkaç yolu vardır:
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

using (FileStream streamIn = new FileStream(MyDir + "Replace regex.docx", FileMode.Open, FileAccess.Read))
{
    ReplacerContext replacerContext = new ReplacerContext();
    replacerContext.SetReplacement(pattern, replacement);
    replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceContextStreamRegex.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Create(replacerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Ayrıca bakınız

* class [ProcessorContext](../processorcontext/)
* ad alanı [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../)
