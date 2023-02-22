---
title: TxtSaveOptionsBase.ForcePageBreaks
second_title: Referencia de API de Aspose.Words para .NET
description: TxtSaveOptionsBase propiedad. Permite especificar si los saltos de página deben conservarse durante la exportación.
type: docs
weight: 30
url: /es/net/aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/
---
## TxtSaveOptionsBase.ForcePageBreaks property

Permite especificar si los saltos de página deben conservarse durante la exportación.

El valor predeterminado es **falso**.

```csharp
public bool ForcePageBreaks { get; set; }
```

### Observaciones

La propiedad afecta solo a los saltos de página que se insertan explícitamente en un documento. No está relacionado con los saltos de página que MS Word inserta automáticamente al final de cada página.

### Ejemplos

Muestra cómo especificar si se deben conservar los saltos de página al exportar un documento a texto sin formato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3");

// Crear un objeto "TxtSaveOptions", que podemos pasar al "Guardar" del documento
// método para modificar cómo guardamos el documento en texto sin formato.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Los objetos "Documento" de Aspose.Words tienen saltos de página, al igual que los documentos de Microsoft Word.
// Los formatos de guardado como ".txt" son un cuerpo de texto continuo sin saltos de página.
// Establezca la propiedad "ForcePageBreaks" en "true" para conservar todos los saltos de página en forma de caracteres '\f'.
// Establezca la propiedad "ForcePageBreaks" en "false" para descartar todos los saltos de página.
saveOptions.ForcePageBreaks = forcePageBreaks;

doc.Save(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt", saveOptions);

// Si cargamos un documento de texto plano con saltos de página,
// el objeto "Documento" los usará para dividir el cuerpo en páginas.
doc = new Document(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt");

Assert.AreEqual(forcePageBreaks ? 3 : 1, doc.PageCount);
```

### Ver también

* class [TxtSaveOptionsBase](../)
* espacio de nombres [Aspose.Words.Saving](../../txtsaveoptionsbase/)
* asamblea [Aspose.Words](../../../)


