---
title: DocumentDirection Enum
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: Aspose.Words para .NET
description: Descubre la enumeración Aspose.Words.DocumentDirection para controlar fácilmente el flujo de texto en tus documentos. ¡Mejora la legibilidad y el formato con esta potente función!
type: docs
weight: 4030
url: /es/net/aspose.words.loading/documentdirection/
---
## DocumentDirection enumeration

Permite especificar la dirección en la que debe fluir el texto en un documento.

```csharp
public enum DocumentDirection
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| LeftToRight | `0` | Dirección de izquierda a derecha. |
| RightToLeft | `1` | Dirección de derecha a izquierda. |
| Auto | `2` | Detección automática de dirección. |

## Ejemplos

Muestra cómo detectar la dirección del texto de un documento de texto sin formato.

```csharp
// Crea un objeto "TxtLoadOptions", que podemos pasar al constructor de un documento
// para modificar la forma en que cargamos un documento de texto plano.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Establezca la propiedad "DocumentDirection" en "DocumentDirection.Auto" detecta automáticamente
// la dirección de cada párrafo de texto que Aspose.Words carga desde texto simple.
//La propiedad "Bidi" de cada párrafo almacenará su dirección.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Detecta texto hebreo de derecha a izquierda.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Detecta texto en inglés de derecha a izquierda.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

### Ver también

* espacio de nombres [Aspose.Words.Loading](../../aspose.words.loading/)
* asamblea [Aspose.Words](../../)
