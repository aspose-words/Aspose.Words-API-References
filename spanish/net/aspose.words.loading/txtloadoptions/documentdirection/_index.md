---
title: TxtLoadOptions.DocumentDirection
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: Aspose.Words para .NET
description: Descubre la propiedad DocumentDirection de TxtLoadOptions para configurar fácilmente la dirección del documento. Optimiza tu diseño con la configuración predeterminada LeftToRight.
type: docs
weight: 50
url: /es/net/aspose.words.loading/txtloadoptions/documentdirection/
---
## TxtLoadOptions.DocumentDirection property

Obtiene o establece una dirección de documento. El valor predeterminado esLeftToRight .

```csharp
public DocumentDirection DocumentDirection { get; set; }
```

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

* enum [DocumentDirection](../../documentdirection/)
* class [TxtLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
