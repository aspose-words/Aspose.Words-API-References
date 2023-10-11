---
title: FieldOptions.PreProcessCulture
second_title: Referencia de API de Aspose.Words para .NET
description: FieldOptions propiedad. Obtiene o establece la cultura para preprocesar los valores de campo.
type: docs
weight: 170
url: /es/net/aspose.words.fields/fieldoptions/preprocessculture/
---
## FieldOptions.PreProcessCulture property

Obtiene o establece la cultura para preprocesar los valores de campo.

```csharp
public CultureInfo PreProcessCulture { get; set; }
```

### Observaciones

Actualmente esta propiedad solo afecta el valor del[`FieldDocProperty`](../../fielddocproperty/) campo.

El valor predeterminado es`nulo` . Cuando esta propiedad se establece en`nulo` , el[`FieldDocProperty`](../../fielddocproperty/)El valor del campo está preprocesado con la cultura controlada por el[`FieldUpdateCultureSource`](../fieldupdateculturesource/) propiedad.

### Ejemplos

Muestra cómo configurar la cultura previa al proceso.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Establece la cultura según la cual algunos campos formatearán sus valores mostrados.
doc.FieldOptions.PreProcessCulture = new CultureInfo("de-DE");

Field field = builder.InsertField(" DOCPROPERTY CreateTime");

// El campo DOCPROPERTY mostrará su resultado formateado de acuerdo con la cultura previa al proceso
// lo hemos configurado en alemán. El campo mostrará la fecha/hora usando el formato "dd.mm.aaaa hh:mm".
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[.]\d{2}[.]\d{4} \d{2}[:]\d{2}").Success);

doc.FieldOptions.PreProcessCulture = CultureInfo.InvariantCulture;
field.Update();

// Después de cambiar a la cultura invariante, el campo DOCPROPERTY utilizará el formato "dd/mm/aaaa hh:mm".
Assert.IsTrue(Regex.Match(field.Result, @"\d{2}[/]\d{2}[/]\d{4} \d{2}[:]\d{2}").Success);
```

### Ver también

* class [FieldOptions](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldoptions/)
* asamblea [Aspose.Words](../../../)


