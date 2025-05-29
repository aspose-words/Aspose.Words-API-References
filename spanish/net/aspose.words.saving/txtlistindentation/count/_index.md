---
title: TxtListIndentation.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words para .NET
description: Descubre la propiedad TxtListIndentation Count para personalizar los niveles de sangría de la lista. Define el número de caracteres que desees para una mejor legibilidad.
type: docs
weight: 30
url: /es/net/aspose.words.saving/txtlistindentation/count/
---
## TxtListIndentation.Count property

Obtiene o establece cuántos[`Character`](../character/)para usar como sangría por cada nivel de lista. El valor predeterminado es 0, lo que significa que no hay sangría.

```csharp
public int Count { get; set; }
```

## Ejemplos

Muestra cómo configurar la sangría de lista al guardar un documento como texto sin formato.

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

// Crea un objeto "TxtSaveOptions", que podemos pasar al método "Guardar" del documento
// para modificar la forma en que guardamos el documento en texto plano.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Establezca la propiedad "Carácter" para asignar un personaje a utilizar
// para relleno que simula la sangría de lista en texto sin formato.
txtSaveOptions.ListIndentation.Character = ' ';

// Establezca la propiedad "Count" para especificar el número de veces
// para colocar el carácter de relleno para cada nivel de sangría de la lista.
txtSaveOptions.ListIndentation.Count = 3;

doc.Save(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt");
string newLine= Environment.NewLine;

Assert.AreEqual($"1. Item 1{newLine}" +
                $"   a. Item 2{newLine}" +
                $"      i. Item 3{newLine}", docText);
```

### Ver también

* class [TxtListIndentation](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
