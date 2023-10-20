---
title: ITextShaperFactory.GetTextShaper
linktitle: GetTextShaper
articleTitle: GetTextShaper
second_title: Aspose.Words para .NET
description: ITextShaperFactory GetTextShaper método. Devuelve una nueva instancia de un modelador de texto para la fuente especificada porfontPath yfaceIndex  en C#.
type: docs
weight: 10
url: /es/net/aspose.words.shaping/itextshaperfactory/gettextshaper/
---
## GetTextShaper(*string, int*) {#gettextshaper_1}

Devuelve una nueva instancia de un modelador de texto para la fuente especificada por*fontPath* y*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontPath, int faceIndex)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fontPath | String | Una ruta absoluta al archivo de fuente. |
| faceIndex | Int32 | Un índice del tipo de fuente en la colección de fuentes TrueType, o 0 si el archivo de fuente especificado no es la colección de fuentes TrueType. |

### Ver también

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* espacio de nombres [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* asamblea [Aspose.Words](../../../)

---

## GetTextShaper(*string, byte[], int*) {#gettextshaper}

Devuelve una nueva instancia de un modelador de texto para la fuente representada por*fontBlob* y*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontId, byte[] fontBlob, int faceIndex)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fontId | String | Un identificador único que se puede asociar de forma única con la fuente proporcionada.*fontBlob* . |
| fontBlob | Byte[] | Matriz de bytes con los datos de fuente. |
| faceIndex | Int32 | Un índice del tipo de fuente en la colección de fuentes TrueType, o 0 si*fontBlob* no es una colección de fuentes TrueType. |

### Ver también

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* espacio de nombres [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* asamblea [Aspose.Words](../../../)
