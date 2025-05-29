---
title: LoadOptions.MswVersion
linktitle: MswVersion
articleTitle: MswVersion
second_title: Aspose.Words para .NET
description: Optimice la carga de documentos con LoadOptions MswVersion. Asegúrese de que sea compatible con versiones específicas de MS Word, utilizando Word 2019 como opción predeterminada para una integración fluida.
type: docs
weight: 100
url: /es/net/aspose.words.loading/loadoptions/mswversion/
---
## LoadOptions.MswVersion property

Permite especificar que el proceso de carga del documento debe coincidir con una versión específica de MS Word. El valor predeterminado esWord2019

```csharp
public MsWordVersion MswVersion { get; set; }
```

## Observaciones

Las diferentes versiones de Word pueden manejar ciertos aspectos del contenido y el formato del documento de manera ligeramente diferente durante el proceso de carga, lo que puede generar pequeñas diferencias en el Modelo de objetos del documento.

## Ejemplos

Muestra cómo emular el procedimiento de carga de una versión específica de Microsoft Word durante la carga de un documento.

```csharp
// De forma predeterminada, Aspose.Words carga documentos según la especificación de Microsoft Word 2019.
LoadOptions loadOptions = new LoadOptions();

Assert.AreEqual(MsWordVersion.Word2019, loadOptions.MswVersion);

//A este documento le falta el estilo de formato de párrafo predeterminado.
//Este estilo predeterminado se regenerará cuando carguemos el documento con Microsoft Word o Aspose.Words.
loadOptions.MswVersion = MsWordVersion.Word2007;
Document doc = new Document(MyDir + "Document.docx", loadOptions);

//El interlineado del estilo tendrá este valor cuando se cargue según la especificación de Microsoft Word 2007.
Assert.AreEqual(12.95d, doc.Styles.DefaultParagraphFormat.LineSpacing, 0.01d);
```

### Ver también

* enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* class [LoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
