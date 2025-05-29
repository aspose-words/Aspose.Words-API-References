---
title: FieldListNum.HasListName
linktitle: HasListName
articleTitle: HasListName
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad FieldListNum HasListName indica si se incluye un nombre de definición de numeración abstracta en el código de campos para mejorar el formato del documento.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldlistnum/haslistname/
---
## FieldListNum.HasListName property

Devuelve un valor que indica si el nombre de una definición de numeración abstracta es proporcionado por el código del campo.

```csharp
public bool HasListName { get; }
```

## Ejemplos

Muestra cómo numerar párrafos con campos LISTNUM.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Los campos LISTNUM muestran un número que se incrementa en cada campo LISTNUM.
//Estos campos también tienen una variedad de opciones que nos permiten usarlos para emular listas numeradas.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// Las listas comienzan a contar en 1 de forma predeterminada, pero podemos establecer este número en un valor diferente, como 0.
//Este campo mostrará "0)".
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

// Los campos LISTNUM mantienen recuentos separados para cada nivel de lista.
// Insertar un campo LISTNUM en el mismo párrafo que otro campo LISTNUM
// aumenta el nivel de la lista en lugar del conteo.
// El siguiente campo continuará el recuento que iniciamos arriba y mostrará un valor de "1" en el nivel de lista 1.
builder.InsertField(FieldType.FieldListNum, true);

// Este campo iniciará un recuento en el nivel de lista 2. Mostrará un valor de "1".
builder.InsertField(FieldType.FieldListNum, true);

// Este campo iniciará un recuento en el nivel de lista 3. Mostrará un valor de "1".
// Los diferentes niveles de lista tienen diferentes formatos,
// por lo que estos campos combinados mostrarán un valor de "1)a)i)".
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// El siguiente campo LISTNUM que insertemos continuará el conteo a nivel de lista
// en el que estaba el campo LISTNUM anterior.
// Podemos usar la propiedad "ListLevel" para saltar a un nivel de lista diferente.
// Si este campo LISTNUM permaneciera en el nivel de lista 3, mostraría "ii)",
// pero, como lo hemos movido al nivel de lista 2, continúa el recuento en ese nivel y muestra "b)".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

//Podemos configurar la propiedad ListName para obtener el campo para emular un tipo de campo AUTONUM diferente.
// "NumberDefault" emula AUTONUM, "OutlineDefault" emula AUTONUMOUT,
// y "LegalDefault" emula los campos AUTONUMLGL.
// El nombre de lista "OutlineDefault" con 1 como número inicial dará como resultado que se muestre "I".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// El ListName no se transfiere del campo anterior, por lo que necesitaremos configurarlo para cada campo nuevo.
//Este campo continúa el conteo con el nombre de lista diferente y muestra "II.".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 5");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.LISTNUM.docx");
```

### Ver también

* class [FieldListNum](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
