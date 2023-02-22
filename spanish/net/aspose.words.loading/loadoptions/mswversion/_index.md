---
title: LoadOptions.MswVersion
second_title: Referencia de API de Aspose.Words para .NET
description: LoadOptions propiedad. Permite especificar que el proceso de carga del documento debe coincidir con una versión específica de MS Word. El valor predeterminado esWord2019
type: docs
weight: 100
url: /es/net/aspose.words.loading/loadoptions/mswversion/
---
## LoadOptions.MswVersion property

Permite especificar que el proceso de carga del documento debe coincidir con una versión específica de MS Word. El valor predeterminado esWord2019

```csharp
public MsWordVersion MswVersion { get; set; }
```

### Observaciones

Las diferentes versiones de Word pueden manejar ciertos aspectos del contenido del documento y el formato de forma ligeramente diferente durante el proceso de carga, lo que puede resultar en diferencias menores en el modelo de objeto del documento.

### Ejemplos

Muestra cómo emular el procedimiento de carga de una versión específica de Microsoft Word durante la carga del documento.

```csharp
// De forma predeterminada, Aspose.Words carga documentos de acuerdo con la especificación de Microsoft Word 2019.
LoadOptions loadOptions = new LoadOptions();

Assert.AreEqual(MsWordVersion.Word2019, loadOptions.MswVersion);

// A este documento le falta el estilo de formato de párrafo predeterminado.
// Este estilo predeterminado se regenerará cuando carguemos el documento ya sea con Microsoft Word o Aspose.Words.
loadOptions.MswVersion = MsWordVersion.Word2007;
Document doc = new Document(MyDir + "Document.docx", loadOptions);

// El espacio entre líneas del estilo tendrá este valor cuando lo cargue la especificación de Microsoft Word 2007.
Assert.AreEqual(12.95d, doc.Styles.DefaultParagraphFormat.LineSpacing, 0.01d);
```

### Ver también

* enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* class [LoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../loadoptions/)
* asamblea [Aspose.Words](../../../)


