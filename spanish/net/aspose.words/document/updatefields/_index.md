---
title: Document.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words para .NET
description: Renueve su documento con el método UpdateFields: actualice de manera eficiente todos los valores de campo para lograr una mayor precisión y una edición fluida.
type: docs
weight: 810
url: /es/net/aspose.words/document/updatefields/
---
## Document.UpdateFields method

Actualiza los valores de los campos en todo el documento.

```csharp
public void UpdateFields()
```

## Observaciones

Cuando abre, modifica y luego guarda un documento, Aspose.Words no actualiza los campos automáticamente, sino que los mantiene intactos. Por lo tanto, generalmente querrá llamar a este método antes de guardar si ha modificado el documento programáticamente y desea asegurarse de que los valores de campo (calculados) adecuados aparezcan en el documento guardado.

No es necesario actualizar los campos después de ejecutar una combinación de correspondencia porque la combinación de correspondencia es un tipo de actualización de campo y actualiza automáticamente todos los campos del documento.

Este método no actualiza todos los tipos de campo. Para obtener una lista detallada de los tipos de campo admitidos, consulte la Guía del programador.

Este método no actualiza los campos relacionados con los algoritmos de diseño de página (por ejemplo, PAGE, PAGES, PAGEREF). Los campos relacionados con el diseño de página se actualizan cuando se representa un documento o se llama a un método.[`UpdatePageLayout`](../updatepagelayout/).

Utilice el[`NormalizeFieldTypes`](../normalizefieldtypes/) método antes de actualizar los campos si hubo cambios en el documento que afectaron los tipos de campo.

Para actualizar campos en una parte específica del documento utilice[`UpdateFields`](../../range/updatefields/).

## Ejemplos

Muestra cómo utilizar el campo QUOTE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte un campo QUOTE, que mostrará el valor de su propiedad Texto.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Inserta un campo QUOTE y anida un campo DATE dentro de él.
// Los campos FECHA actualizan su valor a la fecha actual cada vez que abrimos el documento usando Microsoft Word.
// Anidar el campo FECHA dentro del campo COTIZACIÓN de esta manera congelará su valor
// a la fecha en que creamos el documento.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

//Actualice todos los campos para mostrar sus resultados correctos.
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

// Inserte los campos NOMBRE DE USUARIO, INICIALES DEL USUARIO y DIRECCIÓN DEL USUARIO, que muestran los valores de
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

Muestra cómo insertar una tabla de contenido (TOC) en un documento utilizando estilos de encabezado como entradas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar una tabla de contenidos para la primera página del documento.
// Configurar la tabla para seleccionar párrafos con encabezados de niveles 1 a 3.
// Además, configure sus entradas para que sean hipervínculos que nos llevarán
// a la ubicación del encabezado cuando se hace clic izquierdo en Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Rellene la tabla de contenidos agregando párrafos con estilos de encabezado.
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

// Una tabla de contenidos es un campo de un tipo que necesita actualizarse para mostrar un resultado actualizado.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
