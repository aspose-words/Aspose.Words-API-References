---
title: TxtSaveOptions.SimplifyListLabels
second_title: Referencia de API de Aspose.Words para .NET
description: TxtSaveOptions propiedad. Especifica si el programa debe simplificar las etiquetas de lista en caso de que el formato de etiqueta complejo no se represente adecuadamente mediante texto sin formato.
type: docs
weight: 70
url: /es/net/aspose.words.saving/txtsaveoptions/simplifylistlabels/
---
## TxtSaveOptions.SimplifyListLabels property

Especifica si el programa debe simplificar las etiquetas de lista en caso de que el formato de etiqueta complejo no se represente adecuadamente mediante texto sin formato.

Si se establece en **verdadero** , las etiquetas de listas numeradas se escriben en formato numérico simple y las etiquetas de listas detalladas como caracteres ASCII simples. El valor predeterminado es **falso**.

```csharp
public bool SimplifyListLabels { get; set; }
```

### Ejemplos

Muestra cómo cambiar la apariencia de las listas al guardar un documento en texto sin formato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crear una lista con viñetas con cinco niveles de sangría.
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent();
builder.Writeln("Item 3");
builder.ListFormat.ListIndent();
builder.Writeln("Item 4");
builder.ListFormat.ListIndent();
builder.Write("Item 5");

// Crear un objeto "TxtSaveOptions", que podemos pasar al método "Guardar" del documento
// para modificar cómo guardamos el documento en texto sin formato.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Establecer la propiedad "SimplifyListLabels" en "true" para convertir alguna lista
// símbolos en caracteres ASCII más simples, como '*', 'o', '+', '>', etc.
// Establezca la propiedad "SimplifyListLabels" en "falso" para conservar tantos símbolos de lista originales como sea posible.
txtSaveOptions.SimplifyListLabels = simplifyListLabels;

doc.Save(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt");

if (simplifyListLabels)
    Assert.AreEqual("* Item 1\r\n" +
                    "  > Item 2\r\n" +
                    "    + Item 3\r\n" +
                    "      - Item 4\r\n" +
                    "        o Item 5\r\n", docText);
else
    Assert.AreEqual("· Item 1\r\n" +
                    "o Item 2\r\n" +
                    "§ Item 3\r\n" +
                    "· Item 4\r\n" +
                    "o Item 5\r\n", docText);
```

### Ver también

* class [TxtSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../txtsaveoptions/)
* asamblea [Aspose.Words](../../../)


