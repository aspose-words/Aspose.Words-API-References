---
title: Comparer.Create
linktitle: Create
articleTitle: Create
second_title: .NET için Aspose.Words
description: Dönüştürücü işlemcinin yeni örneklerini daha iyi performans ve verimlilik için oluşturmak üzere Comparer Create yöntemini etkili bir şekilde nasıl kullanacağınızı keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.lowcode/comparer/create/
---
## Create() {#create}

Dönüştürücü işlemcinin yeni bir örneğini oluşturur.

```csharp
public static Comparer Create()
```

### Ayrıca bakınız

* class [Comparer](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## Create(*[ComparerContext](../../comparercontext/)*) {#create_1}

Karşılaştırıcı işlemcinin yeni örneğini oluşturur.

```csharp
public static Comparer Create(ComparerContext context)
```

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

* class [ComparerContext](../../comparercontext/)
* class [Comparer](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)
