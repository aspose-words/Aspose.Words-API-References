---
title: UpdateFields
second_title: Referencia de API de Aspose.Words para .NET
description: Actualiza los valores de los campos en todo el documento.
type: docs
weight: 730
url: /es/net/aspose.words/document/updatefields/
---
## Document.UpdateFields method

Actualiza los valores de los campos en todo el documento.

```csharp
public void UpdateFields()
```

### Observaciones

Cuando abre, modifica y luego guarda un documento, Aspose.Words no actualiza los campos automáticamente, los mantiene intactos. Por lo tanto, normalmente querrá llamar a este método antes de guardar si ha modificado el documento mediante programación y desea asegurarse los valores de campo correctos (calculados) aparecen en el documento guardado.

No es necesario actualizar los campos después de ejecutar una combinación de correspondencia porque la combinación de correspondencia es una especie de actualización de campo y actualiza automáticamente todos los campos del documento.

Este método no actualiza todos los tipos de campo. Para obtener una lista detallada de los tipos de campos admitidos, consulte la Guía del programador.

Este método no actualiza los campos que están relacionados con los algoritmos de diseño de página (por ejemplo, PÁGINA, PÁGINAS, PAGEREF). Los campos relacionados con el diseño de página se actualizan cuando procesa un documento o llama[`UpdatePageLayout`](../updatepagelayout).

Utilizar el[`NormalizeFieldTypes`](../normalizefieldtypes) método antes de actualizar los campos si hubo cambios en el documento que afectaron a los tipos de campo.

Para actualizar campos en una parte específica del documento, use[`UpdateFields`](../../range/updatefields).

### Ejemplos

Muestra para usar el campo COTIZACIÓN.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte un campo COTIZACIÓN, que mostrará el valor de su propiedad Texto.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Inserta un campo de COTIZACIÓN y anida un campo de FECHA dentro de él.
// Los campos FECHA actualizan su valor a la fecha actual cada vez que abrimos el documento usando Microsoft Word.
// Anidar el campo FECHA dentro del campo COTIZACIÓN de esta manera congelará su valor
// hasta la fecha en que creamos el documento.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Actualice todos los campos para mostrar sus resultados correctos.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

Muestra cómo configurar los detalles del usuario y mostrarlos mediante campos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree un objeto UserInformation y configúrelo como fuente de datos para los campos que muestran información del usuario.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// Inserte los campos NOMBRE DE USUARIO, INICIALES DE USUARIO y DIRECCIÓN DE USUARIO, que muestran valores de
// las propiedades respectivas del objeto UserInformation que hemos creado anteriormente. 
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// El objeto de opciones de campo también tiene un usuario predeterminado estático al que pueden hacer referencia los campos de todos los documentos.
UserInformation.DefaultUser.Name = "Default User";
UserInformation.DefaultUser.Initials = "D. U.";
UserInformation.DefaultUser.Address = "One Microsoft Way";
doc.FieldOptions.CurrentUser = UserInformation.DefaultUser;

Assert.AreEqual("Default User", builder.InsertField(" USERNAME ").Result);
Assert.AreEqual("D. U.", builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual("One Microsoft Way", builder.InsertField(" USERADDRESS ").Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.CurrentUser.docx");
```

Muestra cómo insertar una tabla de contenido (TOC) en un documento utilizando estilos de título como entradas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta una tabla de contenido para la primera página del documento.
// Configure la tabla para recoger párrafos con encabezados de niveles 1 a 3.
// Además, configure sus entradas para que sean hipervínculos que nos llevarán
// a la ubicación del encabezado cuando se hace clic con el botón izquierdo en Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Complete la tabla de contenido agregando párrafos con estilos de encabezado.
// Cada encabezado con un nivel entre 1 y 3 creará una entrada en la tabla.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// Una tabla de contenido es un campo de un tipo que debe actualizarse para mostrar un resultado actualizado.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Ver también

* class [Document](../../document)
* espacio de nombres [Aspose.Words](../../document)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
