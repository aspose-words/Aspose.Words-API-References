---
title: Comparer.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words pour .NET
description: Découvrez comment utiliser efficacement la méthode Comparer Create pour générer de nouvelles instances du processeur de convertisseur pour des performances et une efficacité améliorées.
type: docs
weight: 10
url: /fr/net/aspose.words.lowcode/comparer/create/
---
## Create() {#create}

Crée une nouvelle instance du processeur de conversion.

```csharp
public static Comparer Create()
```

### Voir également

* class [Comparer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## Create(*[ComparerContext](../../comparercontext/)*) {#create_1}

Crée une nouvelle instance du processeur comparateur.

```csharp
public static Comparer Create(ComparerContext context)
```

## Exemples

Montre comment comparer simplement des documents en utilisant le contexte.

```csharp
// Il existe plusieurs façons de comparer des documents :
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

Montre comment comparer des documents du flux à l'aide du contexte.

```csharp
// Il existe plusieurs façons de comparer les documents du flux :
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

### Voir également

* class [ComparerContext](../../comparercontext/)
* class [Comparer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
