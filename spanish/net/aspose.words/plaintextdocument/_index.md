---
title: PlainTextDocument Class
linktitle: PlainTextDocument
articleTitle: PlainTextDocument
second_title: Aspose.Words para .NET
description: Aspose.Words.PlainTextDocument clase. Permite extraer la representación en texto plano del contenido del documento en C#.
type: docs
weight: 4440
url: /es/net/aspose.words/plaintextdocument/
---
## PlainTextDocument class

Permite extraer la representación en texto plano del contenido del documento.

Para obtener más información, visite el[Trabajar con documento de texto](https://docs.aspose.com/words/net/working-with-text-document/) artículo de documentación.

```csharp
public class PlainTextDocument
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [PlainTextDocument](plaintextdocument/#constructor)(*Stream*) | Crea un documento de texto sin formato a partir de una secuencia. Detecta automáticamente el formato del archivo. |
| [PlainTextDocument](plaintextdocument/#constructor_2)(*string*) | Crea un documento de texto sin formato a partir de un archivo. Detecta automáticamente el formato del archivo. |
| [PlainTextDocument](plaintextdocument/#constructor_1)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Crea un documento de texto sin formato a partir de una secuencia. Permite especificar opciones adicionales como una contraseña de cifrado. |
| [PlainTextDocument](plaintextdocument/#constructor_3)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Crea un documento de texto sin formato a partir de un archivo. Permite especificar opciones adicionales como una contraseña de cifrado. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BuiltInDocumentProperties](../../aspose.words/plaintextdocument/builtindocumentproperties/) { get; } | Obtiene[`BuiltInDocumentProperties`](./builtindocumentproperties/) del documento. |
| [CustomDocumentProperties](../../aspose.words/plaintextdocument/customdocumentproperties/) { get; } | Obtiene[`CustomDocumentProperties`](./customdocumentproperties/) del documento. |
| [Text](../../aspose.words/plaintextdocument/text/) { get; } | Obtiene el contenido textual del documento concatenado como una cadena. |

## Ejemplos

Muestra cómo cargar el contenido de un documento de Microsoft Word en texto sin formato.

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
