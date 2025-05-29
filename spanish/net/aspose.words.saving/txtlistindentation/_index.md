---
title: TxtListIndentation Class
linktitle: TxtListIndentation
articleTitle: TxtListIndentation
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Saving.TxtListIndentation para personalizar la sangría de las listas y lograr exportaciones fluidas en formato de texto. ¡Mejore el formato de sus documentos!
type: docs
weight: 6450
url: /es/net/aspose.words.saving/txtlistindentation/
---
## TxtListIndentation class

Especifica cómo se sangran los niveles de lista cuando el documento se exporta aText formato.

Para obtener más información, visite el[Guardar un documento](https://docs.aspose.com/words/net/save-a-document/) Artículo de documentación.

```csharp
public class TxtListIndentation
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [TxtListIndentation](txtlistindentation/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Character](../../aspose.words.saving/txtlistindentation/character/) { get; set; } | Obtiene o establece qué carácter utilizar para sangrar los niveles de lista. El valor predeterminado es '\0', lo que significa que no hay sangría. |
| [Count](../../aspose.words.saving/txtlistindentation/count/) { get; set; } | Obtiene o establece cuántos[`Character`](./character/)para usar como sangría por cada nivel de lista. El valor predeterminado es 0, lo que significa que no hay sangría. |

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
