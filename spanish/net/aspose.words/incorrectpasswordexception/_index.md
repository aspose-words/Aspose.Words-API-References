---
title: IncorrectPasswordException Class
linktitle: IncorrectPasswordException
articleTitle: IncorrectPasswordException
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.IncorrectPasswordException, que maneja errores de contraseña para documentos cifrados, lo que garantiza un acceso seguro y sin problemas.
type: docs
weight: 3700
url: /es/net/aspose.words/incorrectpasswordexception/
---
## IncorrectPasswordException class

Se lanza si un documento está encriptado con una contraseña y la contraseña especificada al abrir el documento es incorrecta o falta.

Para obtener más información, visite el[Programación con documentos](https://docs.aspose.com/words/net/programming-with-documents/) Artículo de documentación.

```csharp
public class IncorrectPasswordException : Exception
```

## Ejemplos

Muestra cómo configurar las opciones de guardado para formatos más antiguos de Microsoft Word.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Establezca una contraseña que protegerá la carga del documento por Microsoft Word o Aspose.Words.
// Tenga en cuenta que esto no encripta el contenido del documento de ninguna manera.
options.Password = "MyPassword";

// Si el documento contiene un comprobante de ruta, podemos conservarlo mientras lo guardamos estableciendo este indicador en verdadero.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

//Para poder cargar el documento,
// necesitaremos aplicar la contraseña que especificamos en el objeto DocSaveOptions en un objeto LoadOptions.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
