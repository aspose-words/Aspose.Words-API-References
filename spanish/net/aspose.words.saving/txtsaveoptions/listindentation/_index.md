---
title: TxtSaveOptions.ListIndentation
linktitle: ListIndentation
articleTitle: ListIndentation
second_title: Aspose.Words para .NET
description: TxtSaveOptions ListIndentation propiedad. Obtiene unTxtListIndentation objeto que especifica cuántos y qué caracteres usar para la sangría de los niveles de la lista. De forma predeterminada el recuento del carácter 0 es cero lo que significa que no hay sangría en C#.
type: docs
weight: 30
url: /es/net/aspose.words.saving/txtsaveoptions/listindentation/
---
## TxtSaveOptions.ListIndentation property

Obtiene un[`TxtListIndentation`](../../txtlistindentation/) objeto que especifica cuántos y qué caracteres usar para la sangría de los niveles de la lista. De forma predeterminada, el recuento del carácter '\0' es cero, lo que significa que no hay sangría.

```csharp
public TxtListIndentation ListIndentation { get; }
```

## Ejemplos

Muestra cómo configurar la sangría de lista al guardar un documento en texto sin formato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea una lista con tres niveles de sangría.
builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent(); 
builder.Write("Item 3");

// Crea un objeto "TxtSaveOptions", que podemos pasar al método "Guardar" del documento.
// para modificar cómo guardamos el documento en texto plano.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Establece la propiedad "Carácter" para asignar un carácter a usar
// para relleno que simula la sangría de lista en texto sin formato.
txtSaveOptions.ListIndentation.Character = ' ';

// Establece la propiedad "Count" para especificar el número de veces
// para colocar el carácter de relleno para cada nivel de sangría de la lista.
txtSaveOptions.ListIndentation.Count = 3;

doc.Save(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt");

Assert.AreEqual("1. Item 1\r\n" +
                "   a. Item 2\r\n" +
                "      i. Item 3\r\n", docText);
```

### Ver también

* class [TxtListIndentation](../../txtlistindentation/)
* class [TxtSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
