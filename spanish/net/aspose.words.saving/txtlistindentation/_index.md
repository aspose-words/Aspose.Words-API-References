---
title: Class TxtListIndentation
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.TxtListIndentation clase. Especifica cómo se sangran los niveles de la lista cuando el documento se exporta aText formato.
type: docs
weight: 5370
url: /es/net/aspose.words.saving/txtlistindentation/
---
## TxtListIndentation class

Especifica cómo se sangran los niveles de la lista cuando el documento se exporta aText formato.

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
| [Character](../../aspose.words.saving/txtlistindentation/character/) { get; set; } | Obtiene o establece qué carácter usar para sangrar los niveles de la lista. El valor predeterminado es '\0', lo que significa que no hay sangría. |
| [Count](../../aspose.words.saving/txtlistindentation/count/) { get; set; } | Obtiene o establece cuántos[`Character`](./character/) para usar como sangría por un nivel de lista. El valor predeterminado es 0, eso significa que no hay sangría. |

### Ejemplos

Muestra cómo configurar la sangría de la lista al guardar un documento en texto sin formato.

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

// Crear un objeto "TxtSaveOptions", que podemos pasar al método "Guardar" del documento
// para modificar cómo guardamos el documento en texto sin formato.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Establecer la propiedad "Carácter" para asignar un carácter para usar
// para el relleno que simula la sangría de la lista en texto sin formato.
txtSaveOptions.ListIndentation.Character = ' ';

// Establecer la propiedad "Contar" para especificar el número de veces
// para colocar el carácter de relleno para cada nivel de sangría de la lista.
txtSaveOptions.ListIndentation.Count = 3;

doc.Save(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt");

Assert.AreEqual("1. Item 1\r\n" +
                "   a. Item 2\r\n" +
                "      i. Item 3\r\n", docText);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)


