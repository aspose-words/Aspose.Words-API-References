---
title: TxtSaveOptions.AddBidiMarks
linktitle: AddBidiMarks
articleTitle: AddBidiMarks
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad AddBidiMarks de TxtSaveOptions mejora las exportaciones de texto simple al agregar marcas bidireccionales para mejorar la legibilidad y el formato.
type: docs
weight: 20
url: /es/net/aspose.words.saving/txtsaveoptions/addbidimarks/
---
## TxtSaveOptions.AddBidiMarks property

Especifica si se deben agregar marcas bidireccionales antes de cada ejecución de BiDi al exportar en formato de texto sin formato.

El valor predeterminado es`FALSO`.

```csharp
public bool AddBidiMarks { get; set; }
```

## Ejemplos

Muestra cómo insertar el carácter Unicode 'MARCA DE DERECHA A IZQUIERDA' (U+200F) antes de cada ejecución bidireccional en el texto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.ParagraphFormat.Bidi = true;
builder.Writeln("שלום עולם!");
builder.Writeln("مرحبا بالعالم!");

// Crea un objeto "TxtSaveOptions", que podemos pasar al método "Guardar" del documento
// para modificar la forma en que guardamos el documento en texto plano.
TxtSaveOptions saveOptions = new TxtSaveOptions { Encoding = System.Text.Encoding.Unicode};

// Establezca la propiedad "AddBidiMarks" en "true" para agregar marcas antes de las ejecuciones
// con texto de derecha a izquierda para indicar el hecho.
// Establezca la propiedad "AddBidiMarks" en "falso" para escribir todo de izquierda a derecha
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
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
