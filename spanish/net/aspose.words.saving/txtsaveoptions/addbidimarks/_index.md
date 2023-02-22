---
title: TxtSaveOptions.AddBidiMarks
second_title: Referencia de API de Aspose.Words para .NET
description: TxtSaveOptions propiedad. Especifica si se deben agregar marcas bidireccionales antes de cada ejecución de BiDi al exportar en formato de texto sin formato.
type: docs
weight: 20
url: /es/net/aspose.words.saving/txtsaveoptions/addbidimarks/
---
## TxtSaveOptions.AddBidiMarks property

Especifica si se deben agregar marcas bidireccionales antes de cada ejecución de BiDi al exportar en formato de texto sin formato.

El valor predeterminado es **falso**.

```csharp
public bool AddBidiMarks { get; set; }
```

### Ejemplos

Muestra cómo insertar el carácter Unicode 'MARCA DE DERECHA A IZQUIERDA' (U+200F) antes de cada ejecución bidireccional en el texto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.ParagraphFormat.Bidi = true;
builder.Writeln("שלום עולם!");
builder.Writeln("مرحبا بالعالم!");

// Crear un objeto "TxtSaveOptions", que podemos pasar al método "Guardar" del documento
// para modificar cómo guardamos el documento en texto sin formato.
TxtSaveOptions saveOptions = new TxtSaveOptions { Encoding = System.Text.Encoding.Unicode};

// Establecer la propiedad "AddBidiMarks" en "true" para agregar marcas antes de las ejecuciones
// con texto de derecha a izquierda para indicar el hecho.
// Establecer la propiedad "AddBidiMarks" en "falso" para escribir todo de izquierda a derecha
// y de derecha a izquierda corren igualmente sin nada que indique cuál es cuál.
saveOptions.AddBidiMarks = addBidiMarks;

doc.Save(ArtifactsDir + "TxtSaveOptions.AddBidiMarks.txt", saveOptions);

string docText = System.Text.Encoding.Unicode.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.AddBidiMarks.txt"));

if (addBidiMarks)
{
    Assert.AreEqual("\uFEFFHello world!‎\r\nשלום עולם!‏\r\nمرحبا بالعالم!‏\r\n\r\n", docText);
    Assert.True(docText.Contains("\u200f"));
}
else
{
    Assert.AreEqual("\uFEFFHello world!\r\nשלום עולם!\r\nمرحبا بالعالم!\r\n\r\n", docText);
    Assert.False(docText.Contains("\u200f"));
}
```

### Ver también

* class [TxtSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../txtsaveoptions/)
* asamblea [Aspose.Words](../../../)


