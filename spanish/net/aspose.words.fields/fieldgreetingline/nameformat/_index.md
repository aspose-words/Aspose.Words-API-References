---
title: FieldGreetingLine.NameFormat
second_title: Referencia de API de Aspose.Words para .NET
description: FieldGreetingLine propiedad. Obtiene o establece el formato del nombre incluido en el campo.
type: docs
weight: 40
url: /es/net/aspose.words.fields/fieldgreetingline/nameformat/
---
## FieldGreetingLine.NameFormat property

Obtiene o establece el formato del nombre incluido en el campo.

```csharp
public string NameFormat { get; set; }
```

### Ejemplos

Muestra cómo insertar un campo GREETINGLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un saludo genérico usando un campo GREETINGLINE y algo de texto después.
FieldGreetingLine field = (FieldGreetingLine)builder.InsertField(FieldType.FieldGreetingLine, true);
builder.Writeln("\n\n\tThis is your custom greeting, created programmatically using Aspose Words!");

// Un campo GREETINGLINE acepta valores de una fuente de datos durante una combinación de correspondencia, como MERGEFIELD.
// También puede formatear cómo se escriben los datos de la fuente en su lugar una vez que se completa la combinación de correspondencia.
// La colección de nombres de campos corresponde a las columnas de la fuente de datos
// del que el campo tomará valores.
Assert.AreEqual(0, field.GetFieldNames().Length);

// Para completar esa matriz, necesitamos especificar un formato para nuestra línea de saludo.
field.NameFormat = "<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> ";

// Ahora, nuestro campo aceptará valores de estas dos columnas en la fuente de datos.
Assert.AreEqual("Courtesy Title", field.GetFieldNames()[0]);
Assert.AreEqual("Last Name", field.GetFieldNames()[1]);
Assert.AreEqual(2, field.GetFieldNames().Length);

// Esta cadena cubrirá cualquier caso en el que los datos de la tabla de datos no sean válidos
// sustituyendo el nombre con formato incorrecto por una cadena.
field.AlternateText = "Sir or Madam";

// Establece una configuración regional para formatear el resultado.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(" GREETINGLINE  \\f \"<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> \" \\e \"Sir or Madam\" \\l 1033", 
    field.GetFieldCode());

// Crea una tabla de datos con columnas cuyos nombres coincidan con los elementos
// de la colección de nombres de campo del campo y luego lleve a cabo la combinación de correspondencia.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Esta fila tiene un valor no válido en la columna Título de cortesía, por lo que nuestro saludo utilizará de forma predeterminada el texto alternativo.
table.Rows.Add("", "No", "Name");

doc.MailMerge.Execute(table);

Assert.That(doc.Range.Fields, Is.Empty);
Assert.AreEqual("Dear Mr. Doe,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Mrs. Cardholder,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Sir or Madam,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!",
    doc.GetText().Trim());
```

### Ver también

* class [FieldGreetingLine](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldgreetingline/)
* asamblea [Aspose.Words](../../../)


