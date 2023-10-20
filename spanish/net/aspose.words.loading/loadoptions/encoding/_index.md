---
title: LoadOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words para .NET
description: LoadOptions Encoding propiedad. Obtiene o establece la codificación que se utilizará para cargar un documento HTML TXT o CHM si la codificación no se especifica dentro del documento. Puede sernulo . El valor predeterminado esnulo  en C#.
type: docs
weight: 50
url: /es/net/aspose.words.loading/loadoptions/encoding/
---
## LoadOptions.Encoding property

Obtiene o establece la codificación que se utilizará para cargar un documento HTML, TXT o CHM si la codificación no se especifica dentro del documento. Puede ser`nulo` . El valor predeterminado es`nulo` .

```csharp
public Encoding Encoding { get; set; }
```

## Observaciones

Esta propiedad se utiliza sólo al cargar documentos HTML, TXT o CHM.

Si no se especifica la codificación dentro del documento y esta propiedad es`nulo`entonces el sistema intentará detectar automáticamente la codificación.

## Ejemplos

Muestra cómo configurar la codificación con la que abrir un documento.

```csharp
LoadOptions loadOptions = new LoadOptions
{
    Encoding = Encoding.ASCII
};

// Cargue el documento mientras pasa el objeto LoadOptions, luego verifique el contenido del documento.
Document doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.True(doc.ToString(SaveFormat.Text).Contains("This is a sample text in English."));
```

### Ver también

* class [LoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
