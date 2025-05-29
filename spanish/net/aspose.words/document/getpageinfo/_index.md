---
title: Document.GetPageInfo
linktitle: GetPageInfo
articleTitle: GetPageInfo
second_title: Aspose.Words para .NET
description: Descubra el método GetPageInfo para recuperar detalles esenciales de tamaño de página, orientación y representación para una impresión optimizada y una mejor gestión de documentos.
type: docs
weight: 650
url: /es/net/aspose.words/document/getpageinfo/
---
## Document.GetPageInfo method

Obtiene el tamaño de la página, la orientación y otra información sobre una página que podría ser útil para imprimir o renderizar.

```csharp
public PageInfo GetPageInfo(int pageIndex)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| pageIndex | Int32 | El índice de página basado en 0. |

## Ejemplos

Muestra cómo comprobar si la página está en color o no.

```csharp
Document doc = new Document(MyDir + "Document.docx");

//Verifique que la primera página del documento no esté en color.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### Ver también

* class [PageInfo](../../../aspose.words.rendering/pageinfo/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
