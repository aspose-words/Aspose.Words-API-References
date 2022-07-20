---
title: AppendField
second_title: Referencia de API de Aspose.Words para .NET
description: Agrega un campo a este párrafo.
type: docs
weight: 240
url: /es/net/aspose.words/paragraph/appendfield/
---
## AppendField(FieldType, bool) {#appendfield}

Agrega un campo a este párrafo.

```csharp
public Field AppendField(FieldType fieldType, bool updateField)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fieldType | FieldType | El tipo del campo a agregar. |
| updateField | Boolean | Especifica si actualizar el campo inmediatamente. |

### Valor_devuelto

A[`Field`](../../../aspose.words.fields/field) objeto que representa el campo adjunto.

### Ejemplos

Muestra varias formas de añadir campos a un párrafo.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// A continuación se muestran tres formas de agregar un campo al final de un párrafo.
// 1 - Agregue un campo de FECHA usando un tipo de campo y luego actualícelo:
paragraph.AppendField(FieldType.FieldDate, true);

// 2 - Agrega un campo HORA usando un código de campo: 
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Agregue un campo COTIZACIÓN usando un código de campo y haga que muestre un valor de marcador de posición:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Este campo mostrará su valor de marcador de posición hasta que lo actualicemos.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Ver también

* class [Field](../../../aspose.words.fields/field)
* enum [FieldType](../../../aspose.words.fields/fieldtype)
* class [Paragraph](../../paragraph)
* espacio de nombres [Aspose.Words](../../paragraph)
* asamblea [Aspose.Words](../../../)

---

## AppendField(string) {#appendfield_1}

Agrega un campo a este párrafo.

```csharp
public Field AppendField(string fieldCode)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fieldCode | String | El código de campo para agregar (sin llaves). |

### Valor_devuelto

A[`Field`](../../../aspose.words.fields/field) objeto que representa el campo adjunto.

### Ejemplos

Muestra varias formas de añadir campos a un párrafo.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// A continuación se muestran tres formas de agregar un campo al final de un párrafo.
// 1 - Agregue un campo de FECHA usando un tipo de campo y luego actualícelo:
paragraph.AppendField(FieldType.FieldDate, true);

// 2 - Agrega un campo HORA usando un código de campo: 
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Agregue un campo COTIZACIÓN usando un código de campo y haga que muestre un valor de marcador de posición:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Este campo mostrará su valor de marcador de posición hasta que lo actualicemos.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Ver también

* class [Field](../../../aspose.words.fields/field)
* class [Paragraph](../../paragraph)
* espacio de nombres [Aspose.Words](../../paragraph)
* asamblea [Aspose.Words](../../../)

---

## AppendField(string, string) {#appendfield_2}

Agrega un campo a este párrafo.

```csharp
public Field AppendField(string fieldCode, string fieldValue)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fieldCode | String | El código de campo para agregar (sin llaves). |
| fieldValue | String | El valor del campo a agregar. Pase nulo para los campos que no tienen un valor. |

### Valor_devuelto

A[`Field`](../../../aspose.words.fields/field) objeto que representa el campo adjunto.

### Ejemplos

Muestra varias formas de añadir campos a un párrafo.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// A continuación se muestran tres formas de agregar un campo al final de un párrafo.
// 1 - Agregue un campo de FECHA usando un tipo de campo y luego actualícelo:
paragraph.AppendField(FieldType.FieldDate, true);

// 2 - Agrega un campo HORA usando un código de campo: 
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Agregue un campo COTIZACIÓN usando un código de campo y haga que muestre un valor de marcador de posición:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Este campo mostrará su valor de marcador de posición hasta que lo actualicemos.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Ver también

* class [Field](../../../aspose.words.fields/field)
* class [Paragraph](../../paragraph)
* espacio de nombres [Aspose.Words](../../paragraph)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
