---
title: Comparer.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words para .NET
description: Descubra cómo utilizar eficazmente el método Comparer Create para generar nuevas instancias del procesador del convertidor para mejorar el rendimiento y la eficiencia.
type: docs
weight: 10
url: /es/net/aspose.words.lowcode/comparer/create/
---
## Create() {#create}

Crea una nueva instancia del procesador del convertidor.

```csharp
public static Comparer Create()
```

### Ver también

* class [Comparer](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## Create(*[ComparerContext](../../comparercontext/)*) {#create_1}

Crea una nueva instancia del procesador comparador.

```csharp
public static Comparer Create(ComparerContext context)
```

## Ejemplos

Muestra cómo comparar documentos de forma sencilla utilizando el contexto.

```csharp
//Hay varias formas de comparar documentos:
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

Muestra cómo comparar documentos de la secuencia utilizando el contexto.

```csharp
// Hay varias formas de comparar documentos de la secuencia:
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

### Ver también

* class [ComparerContext](../../comparercontext/)
* class [Comparer](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
