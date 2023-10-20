---
title: TxtLoadOptions.DocumentDirection
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: Aspose.Words para .NET
description: TxtLoadOptions DocumentDirection propiedad. Obtiene o establece una dirección del documento. El valor predeterminado esLeftToRight  en C#.
type: docs
weight: 40
url: /es/net/aspose.words.loading/txtloadoptions/documentdirection/
---
## TxtLoadOptions.DocumentDirection property

Obtiene o establece una dirección del documento. El valor predeterminado esLeftToRight .

```csharp
public DocumentDirection DocumentDirection { get; set; }
```

## Ejemplos

Muestra cómo detectar la dirección del texto de un documento sin formato.

```csharp
// Crea un objeto "TxtLoadOptions", que podemos pasar al constructor de un documento.
// para modificar cómo cargamos un documento de texto plano.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Establece la propiedad "DocumentDirection" en "DocumentDirection.Auto" detecta automáticamente
// la dirección de cada párrafo de texto que Aspose.Words carga desde texto sin formato.
// La propiedad "Bidi" de cada párrafo almacenará su dirección.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Detecta texto hebreo de derecha a izquierda.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Detecta texto en inglés de derecha a izquierda.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

### Ver también

* enum [DocumentDirection](../../documentdirection/)
* class [TxtLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
