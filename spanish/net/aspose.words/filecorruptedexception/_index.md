---
title: FileCorruptedException Class
linktitle: FileCorruptedException
articleTitle: FileCorruptedException
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.FileCorruptedException, diseñada para gestionar fácilmente documentos dañados durante la carga. ¡Asegure una gestión fluida de documentos!
type: docs
weight: 3210
url: /es/net/aspose.words/filecorruptedexception/
---
## FileCorruptedException class

Se lanza durante la carga del documento, cuando el documento parece estar dañado y es imposible cargarlo.

Para obtener más información, visite el[Programación con documentos](https://docs.aspose.com/words/net/programming-with-documents/) Artículo de documentación.

```csharp
public class FileCorruptedException : Exception
```

## Ejemplos

Muestra cómo detectar una FileCorruptedException.

```csharp
try
{
    // Si recibimos un mensaje de error de "Contenido ilegible" al intentar abrir un documento con Microsoft Word,
    // lo más probable es que se produzca una excepción al intentar cargar ese documento usando Aspose.Words.
    Document doc = new Document(MyDir + "Corrupted document.docx");
}
catch (FileCorruptedException e)
{
    Console.WriteLine(e.Message);
}
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
