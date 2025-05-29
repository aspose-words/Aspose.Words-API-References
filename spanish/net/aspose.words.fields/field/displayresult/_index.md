---
title: Field.DisplayResult
linktitle: DisplayResult
articleTitle: DisplayResult
second_title: Aspose.Words para .NET
description: Descubra la propiedad Field DisplayResult que entrega el texto de los resultados de campo mostrados, mejorando la claridad y la experiencia del usuario.
type: docs
weight: 10
url: /es/net/aspose.words.fields/field/displayresult/
---
## Field.DisplayResult property

Obtiene el texto que representa el resultado del campo mostrado.

```csharp
public string DisplayResult { get; }
```

## Observaciones

El[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) Se debe llamar al método para obtener el valor correcto para the [`FieldListNum`](../../fieldlistnum/) ,[`FieldAutoNum`](../../fieldautonum/) ,[`FieldAutoNumOut`](../../fieldautonumout/) y[`FieldAutoNumLgl`](../../fieldautonumlgl/) campos.

## Ejemplos

Muestra cómo obtener el texto real que muestra un campo en el documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This document was written by ");
FieldAuthor fieldAuthor = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
fieldAuthor.AuthorName = "John Doe";

// Podemos usar la propiedad DisplayResult para verificar qué texto exacto
// un campo se mostraría en su lugar en el documento.
Assert.AreEqual(string.Empty, fieldAuthor.DisplayResult);

 //Los campos no mantienen valores de resultados precisos en tiempo real.
// Para garantizar que nuestros campos muestren resultados precisos en cualquier momento,
// por ejemplo, justo antes de una operación de guardado, necesitamos actualizarlos manualmente.
fieldAuthor.Update();

Assert.AreEqual("John Doe", fieldAuthor.DisplayResult);

doc.Save(ArtifactsDir + "Field.DisplayResult.docx");
```

### Ver también

* class [Field](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
