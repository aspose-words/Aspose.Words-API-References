---
title: FileCorruptedException Class
linktitle: FileCorruptedException
articleTitle: FileCorruptedException
second_title: Aspose.Words para .NET
description: Aspose.Words.FileCorruptedException clase. Se produce durante la carga del documento cuando el documento parece estar dañado y es imposible cargarlo en C#.
type: docs
weight: 2800
url: /es/net/aspose.words/filecorruptedexception/
---
## FileCorruptedException class

Se produce durante la carga del documento, cuando el documento parece estar dañado y es imposible cargarlo.

Para obtener más información, visite el[Programación con documentos](https://docs.aspose.com/words/net/programming-with-documents/) artículo de documentación.

```csharp
public class FileCorruptedException : Exception
```

## Ejemplos

Muestra cómo detectar una FileCorruptedException.

```csharp
try
{
    // Si recibimos un mensaje de error "Contenido ilegible" al intentar abrir un documento usando Microsoft Word,
    // lo más probable es que obtengamos una excepción al intentar cargar ese documento usando Aspose.Words.
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
