---
title: ImageFieldMergingArgs.Shape
linktitle: Shape
articleTitle: Shape
second_title: Aspose.Words per .NET
description: ImageFieldMergingArgs Shape proprietà. Specifica la forma che il motore di stampa unione deve inserire nel documento in C#.
type: docs
weight: 60
url: /it/net/aspose.words.mailmerging/imagefieldmergingargs/shape/
---
## ImageFieldMergingArgs.Shape property

Specifica la forma che il motore di stampa unione deve inserire nel documento.

```csharp
public Shape Shape { get; set; }
```

## Osservazioni

Quando questa proprietà è specificata, il motore di stampa unione ignora tutte le altre proprietà come[`ImageFileName`](../imagefilename/) O[`ImageStream`](../imagestream/) e inserisce semplicemente la forma nel documento.

Utilizza questa proprietà per controllare completamente il processo di unione di un campo di unione immagine. Ad esempio, puoi specificare[`WrapType`](../../../aspose.words.drawing/shapebase/wraptype/) o qualsiasi altra proprietà della forma per mettere a punto il nodo risultante. Tuttavia, tieni presente che sei responsabile di fornire il contenuto della forma.

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* class [ImageFieldMergingArgs](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
