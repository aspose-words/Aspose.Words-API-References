---
title: TxtSaveOptionsBase.ForcePageBreaks
linktitle: ForcePageBreaks
articleTitle: ForcePageBreaks
second_title: Aspose.Words para .NET
description: Controle los saltos de página con la propiedad ForcePageBreaks de TxtSaveOptionsBase. Asegúrese de que las exportaciones sean fluidas y mantenga el formato del documento sin problemas.
type: docs
weight: 30
url: /es/net/aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/
---
## TxtSaveOptionsBase.ForcePageBreaks property

Permite especificar si los saltos de página deben conservarse durante la exportación.

El valor predeterminado es`FALSO`.

```csharp
public bool ForcePageBreaks { get; set; }
```

## Observaciones

La propiedad afecta únicamente a los saltos de página que se insertan explícitamente en un documento. No está relacionada con los saltos de página que MS Word inserta automáticamente al final de cada página.

## Ejemplos

Muestra cómo especificar si se deben conservar los saltos de página al exportar un documento a texto sin formato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3");

// Crea un objeto "TxtSaveOptions", que podemos pasar al "Guardar" del documento
// método para modificar la forma en que guardamos el documento en texto plano.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Los objetos "Documento" de Aspose.Words tienen saltos de página, al igual que los documentos de Microsoft Word.
// Los formatos guardados como ".txt" son un cuerpo continuo de texto sin saltos de página.
// Establezca la propiedad "ForcePageBreaks" en "true" para conservar todos los saltos de página en forma de caracteres '\f'.
// Establezca la propiedad "ForcePageBreaks" en "false" para descartar todos los saltos de página.
saveOptions.ForcePageBreaks = forcePageBreaks;

doc.Save(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt", saveOptions);

// Si cargamos un documento de texto plano con saltos de página,
// El objeto "Documento" los usará para dividir el cuerpo en páginas.
doc = new Document(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt");

Assert.AreEqual(forcePageBreaks ? 3 : 1, doc.PageCount);
```

### Ver también

* class [TxtSaveOptionsBase](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
