---
title: Paragraph.AppendField
linktitle: AppendField
articleTitle: AppendField
second_title: Aspose.Words para .NET
description: Mejore su documento con el método Paragraph AppendField, agregando sin problemas campos personalizados a los párrafos para mejorar la organización y la claridad.
type: docs
weight: 260
url: /es/net/aspose.words/paragraph/appendfield/
---
## AppendField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool*) {#appendfield}

Agrega un campo a este párrafo.

```csharp
public Field AppendField(FieldType fieldType, bool updateField)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fieldType | FieldType | El tipo de campo a agregar. |
| updateField | Boolean | Especifica si se debe actualizar el campo inmediatamente. |

### Valor_devuelto

A[`Field`](../../../aspose.words.fields/field/) objeto que representa el campo añadido.

## Ejemplos

Muestra varias formas de agregar campos a un párrafo.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// A continuación se muestran tres formas de agregar un campo al final de un párrafo.
// 1 - Agregue un campo FECHA usando un tipo de campo y luego actualícelo:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - Agrega un campo TIME usando un código de campo:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Agregue un campo QUOTE usando un código de campo y haga que muestre un valor de marcador de posición:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Este campo mostrará su valor de marcador de posición hasta que lo actualicemos.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Ver también

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## AppendField(*string*) {#appendfield_1}

Agrega un campo a este párrafo.

```csharp
public Field AppendField(string fieldCode)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fieldCode | String | El código de campo a agregar (sin llaves). |

### Valor_devuelto

A[`Field`](../../../aspose.words.fields/field/) objeto que representa el campo añadido.

## Ejemplos

Muestra varias formas de agregar campos a un párrafo.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// A continuación se muestran tres formas de agregar un campo al final de un párrafo.
// 1 - Agregue un campo FECHA usando un tipo de campo y luego actualícelo:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - Agrega un campo TIME usando un código de campo:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Agregue un campo QUOTE usando un código de campo y haga que muestre un valor de marcador de posición:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Este campo mostrará su valor de marcador de posición hasta que lo actualicemos.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Ver también

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## AppendField(*string, string*) {#appendfield_2}

Agrega un campo a este párrafo.

```csharp
public Field AppendField(string fieldCode, string fieldValue)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fieldCode | String | El código de campo a agregar (sin llaves). |
| fieldValue | String | El valor del campo que se va a añadir. Pasar`nulo` para campos que no tienen un valor. |

### Valor_devuelto

A[`Field`](../../../aspose.words.fields/field/) objeto que representa el campo añadido.

## Ejemplos

Muestra varias formas de agregar campos a un párrafo.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// A continuación se muestran tres formas de agregar un campo al final de un párrafo.
// 1 - Agregue un campo FECHA usando un tipo de campo y luego actualícelo:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - Agrega un campo TIME usando un código de campo:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Agregue un campo QUOTE usando un código de campo y haga que muestre un valor de marcador de posición:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Este campo mostrará su valor de marcador de posición hasta que lo actualicemos.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Ver también

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
