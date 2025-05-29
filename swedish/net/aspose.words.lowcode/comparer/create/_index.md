---
title: Comparer.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words för .NET
description: Upptäck hur du effektivt använder Comparer Create-metoden för att generera nya instanser av konverteringsprocessorn för förbättrad prestanda och effektivitet.
type: docs
weight: 10
url: /sv/net/aspose.words.lowcode/comparer/create/
---
## Create() {#create}

Skapar en ny instans av konverteringsprocessorn.

```csharp
public static Comparer Create()
```

### Se även

* class [Comparer](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Create(*[ComparerContext](../../comparercontext/)*) {#create_1}

Skapar en ny instans av jämförarprocessorn.

```csharp
public static Comparer Create(ComparerContext context)
```

## Exempel

Visar hur man enkelt jämför dokument med hjälp av kontext.

```csharp
// Det finns flera sätt att jämföra dokument:
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

Visar hur man jämför dokument från strömmen med hjälp av kontext.

```csharp
// Det finns flera sätt att jämföra dokument från strömmen:
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

### Se även

* class [ComparerContext](../../comparercontext/)
* class [Comparer](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
