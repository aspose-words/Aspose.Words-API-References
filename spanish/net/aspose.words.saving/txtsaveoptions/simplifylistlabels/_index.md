---
title: TxtSaveOptions.SimplifyListLabels
linktitle: SimplifyListLabels
articleTitle: SimplifyListLabels
second_title: Aspose.Words para .NET
description: Descubra cómo la función SimplifyListLabels de TxtSaveOptions mejora la claridad al simplificar las etiquetas de listas complejas para una mejor representación del texto.
type: docs
weight: 70
url: /es/net/aspose.words.saving/txtsaveoptions/simplifylistlabels/
---
## TxtSaveOptions.SimplifyListLabels property

Especifica si el programa debe simplificar las etiquetas de lista en caso de que el formato de etiqueta complejo no esté representado adecuadamente por texto simple.

Si se establece en`verdadero` Las etiquetas de las listas numeradas se escriben en formato numérico simple y las etiquetas de las listas detalladas, como caracteres ASCII simples. El valor predeterminado es`FALSO`.

```csharp
public bool SimplifyListLabels { get; set; }
```

## Ejemplos

Muestra cómo cambiar la apariencia de las listas al guardar un documento en texto sin formato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea una lista con viñetas con cinco niveles de sangría.
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

// Crea un objeto "TxtSaveOptions", que podemos pasar al método "Guardar" del documento
// para modificar la forma en que guardamos el documento en texto plano.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Establezca la propiedad "SimplifyListLabels" en "verdadero" para convertir alguna lista
// símbolos en caracteres ASCII más simples, como '*', 'o', '+', '>', etc.
// Establezca la propiedad "SimplifyListLabels" en "falso" para conservar tantos símbolos de lista originales como sea posible.
txtSaveOptions.SimplifyListLabels = simplifyListLabels;

doc.Save(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt");

string newLine = Environment.NewLine;

if (simplifyListLabels)
    Assert.AreEqual($"* Item 1{newLine}" +
                    $"  > Item 2{newLine}" +
                    $"    + Item 3{newLine}" +
                    $"      - Item 4{newLine}" +
                    $"        o Item 5{newLine}", docText);
else
    Assert.AreEqual($"· Item 1{newLine}" +
                    $"o Item 2{newLine}" +
                    $"§ Item 3{newLine}" +
                    $"· Item 4{newLine}" +
                    $"o Item 5{newLine}", docText);
```

### Ver también

* class [TxtSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
