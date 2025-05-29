---
title: ComparerContext Class
linktitle: ComparerContext
articleTitle: ComparerContext
second_title: .NET için Aspose.Words
description: Verimli belge karşılaştırması için Aspose.Words LowCode ComparerContext sınıfını keşfedin, kusursuz entegrasyon ve güçlü özelliklerle iş akışınızı geliştirin.
type: docs
weight: 4220
url: /tr/net/aspose.words.lowcode/comparercontext/
---
## ComparerContext class

Belge karşılaştırıcı bağlamı

```csharp
public class ComparerContext : ProcessorContext
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [ComparerContext](comparercontext/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AcceptRevisions](../../aspose.words.lowcode/comparercontext/acceptrevisions/) { get; set; } | Belgeleri karşılaştırmadan önce revizyonların kabul edilip edilmeyeceğini belirtir. Karşılaştırılan belgeler revizyonlar içeriyorsa ve bu bayrak false olarak ayarlanırsa, işlemci revizyonları reddeder. Varsayılan`doğru` . |
| [Author](../../aspose.words.lowcode/comparercontext/author/) { get; set; } | Belge karşılaştırması sırasında oluşturulan revizyonlara atanacak yazar. |
| [CompareOptions](../../aspose.words.lowcode/comparercontext/compareoptions/) { get; } | Belgeleri karşılaştırırken kullanılan seçenekler. |
| [DateTime](../../aspose.words.lowcode/comparercontext/datetime/) { get; set; } | Belge karşılaştırması sırasında oluşturulan revizyonlara atanan tarih ve saat. |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | İşlemci tarafından kullanılan yazı tipi ayarları. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | İşlemci tarafından kullanılan belge düzeni seçenekleri. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | İşlemci tarafından kullanılan uyarı geri araması. |

## Örnekler

Belgelerin bağlam kullanılarak nasıl basit bir şekilde karşılaştırılacağını gösterir.

```csharp
// Belgeleri karşılaştırmanın birkaç yolu vardır:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

ComparerContext comparerContext = new ComparerContext();
comparerContext.CompareOptions.IgnoreCaseChanges = true;
comparerContext.Author = "Author";
comparerContext.DateTime = new DateTime();

Comparer.Create(comparerContext)
    .From(firstDoc)
    .From(secondDoc)
    .To(ArtifactsDir + "LowCode.CompareContextDocuments.docx")
    .Execute();
```

Akıştaki belgelerin bağlam kullanılarak nasıl karşılaştırılacağını gösterir.

```csharp
// Akıştaki belgeleri karşılaştırmanın birkaç yolu vardır:
using (FileStream firstStreamIn = new FileStream(MyDir + "Table column bookmarks.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Table column bookmarks.doc", FileMode.Open, FileAccess.Read))
    {
        ComparerContext comparerContext = new ComparerContext();
        comparerContext.CompareOptions.IgnoreCaseChanges = true;
        comparerContext.Author = "Author";
        comparerContext.DateTime = new DateTime();

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareContextStreamDocuments.docx", FileMode.Create, FileAccess.ReadWrite))
            Comparer.Create(comparerContext)
                .From(firstStreamIn)
                .From(secondStreamIn)
                .To(streamOut, SaveFormat.Docx)
                .Execute();
    }
}
```

### Ayrıca bakınız

* class [ProcessorContext](../processorcontext/)
* ad alanı [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../)
