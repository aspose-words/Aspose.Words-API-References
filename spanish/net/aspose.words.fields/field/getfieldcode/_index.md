---
title: Field.GetFieldCode
linktitle: GetFieldCode
articleTitle: GetFieldCode
second_title: Aspose.Words para .NET
description: Descubra el método GetFieldCode y recupere fácilmente el texto entre el inicio y el separador del campo, incluyendo los códigos de los campos secundarios y los resultados. ¡Mejore su eficiencia de codificación!
type: docs
weight: 110
url: /es/net/aspose.words.fields/field/getfieldcode/
---
## GetFieldCode() {#getfieldcode}

Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Se incluyen tanto el código de campo como el resultado de campo de los campos secundarios.

```csharp
public string GetFieldCode()
```

## Ejemplos

Muestra cómo insertar un campo en un documento utilizando un código de campo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Esta sobrecarga del método InsertField actualiza automáticamente los campos insertados.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

Muestra cómo obtener el código de campo de un campo.

```csharp
//Abre un documento que contiene un MERGEFIELD dentro de un campo IF.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// Hay dos formas de obtener el código de campo de un campo:
// 1 - Omitir sus campos internos:
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - Incluya sus campos internos:
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// De forma predeterminada, el método GetFieldCode muestra los campos internos.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### Ver también

* class [Field](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)

---

## GetFieldCode(*bool*) {#getfieldcode_1}

Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador).

```csharp
public string GetFieldCode(bool includeChildFieldCodes)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| includeChildFieldCodes | Boolean | `verdadero` Si se deben incluir los códigos de campo secundarios. |

## Ejemplos

Muestra cómo obtener el código de campo de un campo.

```csharp
//Abre un documento que contiene un MERGEFIELD dentro de un campo IF.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// Hay dos formas de obtener el código de campo de un campo:
// 1 - Omitir sus campos internos:
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - Incluya sus campos internos:
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// De forma predeterminada, el método GetFieldCode muestra los campos internos.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### Ver también

* class [Field](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
