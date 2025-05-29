---
title: FieldBuilder
linktitle: FieldBuilder
articleTitle: FieldBuilder
second_title: Aspose.Words para .NET
description: Descubre FieldBuilder, la potente herramienta para crear y gestionar campos en tus proyectos sin esfuerzo. ¡Optimiza tu flujo de trabajo hoy mismo!
type: docs
weight: 10
url: /es/net/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder constructor

Inicializa una instancia de la[`FieldBuilder`](../) clase.

```csharp
public FieldBuilder(FieldType fieldType)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fieldType | FieldType | El tipo de campo a construir. |

## Ejemplos

Muestra cómo crear e insertar un campo utilizando un generador de campos.

```csharp
Document doc = new Document();

// Una forma conveniente de agregar contenido de texto a un documento es con un generador de documentos.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write(" Hello world! This text is one Run, which is an inline node.");

// Los campos tienen su constructor, el cual podemos usar para construir un código de campo pieza por pieza.
// En este caso, construiremos un campo CÓDIGO DE BARRAS que represente un código postal de EE. UU.,
// y luego insertarlo delante de un Run.
FieldBuilder fieldBuilder = new FieldBuilder(FieldType.FieldBarcode);
fieldBuilder.AddArgument("90210");
fieldBuilder.AddSwitch("\\f", "A");
fieldBuilder.AddSwitch("\\u");

fieldBuilder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph.Runs[0]);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CreateWithFieldBuilder.docx");
```

### Ver también

* enum [FieldType](../../fieldtype/)
* class [FieldBuilder](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
