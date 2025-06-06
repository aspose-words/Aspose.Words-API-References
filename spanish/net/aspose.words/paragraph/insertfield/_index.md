---
title: Paragraph.InsertField
linktitle: InsertField
articleTitle: InsertField
second_title: Aspose.Words para .NET
description: Inserte campos fácilmente en párrafos con el método InsertarCampo de Párrafo. Mejore la funcionalidad de su documento y agilice la gestión de contenido.
type: docs
weight: 290
url: /es/net/aspose.words/paragraph/insertfield/
---
## InsertField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool, [Node](../../node/), bool*) {#insertfield}

Inserta un campo en este párrafo.

```csharp
public Field InsertField(FieldType fieldType, bool updateField, Node refNode, bool isAfter)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fieldType | FieldType | El tipo de campo a insertar. |
| updateField | Boolean | Especifica si se debe actualizar el campo inmediatamente. |
| refNode | Node | Nodo de referencia dentro de este párrafo (si*refNode* es`nulo`, luego se añade al final del párrafo). |
| isAfter | Boolean | Si insertar el campo después o antes del nodo de referencia. |

### Valor_devuelto

A[`Field`](../../../aspose.words.fields/field/) objeto que representa el campo insertado.

## Ejemplos

Muestra varias formas de agregar campos a un párrafo.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// A continuación se muestran tres formas de insertar un campo en un párrafo.
// 1 - Inserta un campo AUTOR en un párrafo después de uno de los nodos secundarios del párrafo:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Insertar un campo QUOTE después de uno de los nodos secundarios del párrafo:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Insertar un campo QUOTE antes de uno de los nodos secundarios del párrafo,
// y hacer que muestre un valor de marcador de posición:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Este campo mostrará su valor de marcador de posición hasta que lo actualicemos.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Ver también

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Node](../../node/)
* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertField(*string, [Node](../../node/), bool*) {#insertfield_1}

Inserta un campo en este párrafo.

```csharp
public Field InsertField(string fieldCode, Node refNode, bool isAfter)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fieldCode | String | El código de campo a insertar (sin llaves). |
| refNode | Node | Nodo de referencia dentro de este párrafo (si*refNode* es`nulo`, luego se añade al final del párrafo). |
| isAfter | Boolean | Si insertar el campo después o antes del nodo de referencia. |

### Valor_devuelto

A[`Field`](../../../aspose.words.fields/field/) objeto que representa el campo insertado.

## Ejemplos

Muestra varias formas de agregar campos a un párrafo.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// A continuación se muestran tres formas de insertar un campo en un párrafo.
// 1 - Inserta un campo AUTOR en un párrafo después de uno de los nodos secundarios del párrafo:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Insertar un campo QUOTE después de uno de los nodos secundarios del párrafo:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Insertar un campo QUOTE antes de uno de los nodos secundarios del párrafo,
// y hacer que muestre un valor de marcador de posición:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Este campo mostrará su valor de marcador de posición hasta que lo actualicemos.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Ver también

* class [Field](../../../aspose.words.fields/field/)
* class [Node](../../node/)
* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertField(*string, string, [Node](../../node/), bool*) {#insertfield_2}

Inserta un campo en este párrafo.

```csharp
public Field InsertField(string fieldCode, string fieldValue, Node refNode, bool isAfter)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fieldCode | String | El código de campo a insertar (sin llaves). |
| fieldValue | String | El valor del campo a insertar. Pasar`nulo` para campos que no tienen un valor. |
| refNode | Node | Nodo de referencia dentro de este párrafo (si*refNode* es`nulo`, luego se añade al final del párrafo). |
| isAfter | Boolean | Si insertar el campo después o antes del nodo de referencia. |

### Valor_devuelto

A[`Field`](../../../aspose.words.fields/field/) objeto que representa el campo insertado.

## Ejemplos

Muestra varias formas de agregar campos a un párrafo.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// A continuación se muestran tres formas de insertar un campo en un párrafo.
// 1 - Inserta un campo AUTOR en un párrafo después de uno de los nodos secundarios del párrafo:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Insertar un campo QUOTE después de uno de los nodos secundarios del párrafo:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Insertar un campo QUOTE antes de uno de los nodos secundarios del párrafo,
// y hacer que muestre un valor de marcador de posición:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Este campo mostrará su valor de marcador de posición hasta que lo actualicemos.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Ver también

* class [Field](../../../aspose.words.fields/field/)
* class [Node](../../node/)
* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
