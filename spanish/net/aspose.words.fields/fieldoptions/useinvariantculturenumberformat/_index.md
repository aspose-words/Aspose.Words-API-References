---
title: FieldOptions.UseInvariantCultureNumberFormat
linktitle: UseInvariantCultureNumberFormat
articleTitle: UseInvariantCultureNumberFormat
second_title: Aspose.Words para .NET
description: FieldOptions UseInvariantCultureNumberFormat propiedad. Obtiene o establece el valor que indica que el formato del número se analiza utilizando una cultura invariante o no en C#.
type: docs
weight: 210
url: /es/net/aspose.words.fields/fieldoptions/useinvariantculturenumberformat/
---
## FieldOptions.UseInvariantCultureNumberFormat property

Obtiene o establece el valor que indica que el formato del número se analiza utilizando una cultura invariante o no

```csharp
public bool UseInvariantCultureNumberFormat { get; set; }
```

## Observaciones

Cuando esta propiedad se establece en`verdadero` , el formato numérico se toma de una cultura invariante.

Cuando esta propiedad se establece en`FALSO` , el formato del número se toma de la cultura del hilo actual.

El valor predeterminado es`FALSO`.

## Ejemplos

Muestra cómo formatear números según la cultura invariante.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Thread.CurrentThread.CurrentCulture = new CultureInfo("de-DE");
Field field = builder.InsertField(" = 1234567,89 \\# $#,###,###.##");
field.Update();

 // A veces, es posible que los campos no formaten sus números correctamente en determinadas culturas.
Assert.IsFalse(doc.FieldOptions.UseInvariantCultureNumberFormat);
Assert.AreEqual("$1234567,89 .     ", field.Result);

// Para solucionar este problema, podríamos cambiar la cultura de todo el hilo.
// Otra forma de solucionar este problema es establecer este indicador,
// que hace que todos los campos utilicen la cultura invariante al formatear números.
// De esta manera nos permite evitar cambiar la cultura de todo el hilo.
doc.FieldOptions.UseInvariantCultureNumberFormat = true;
field.Update();
Assert.AreEqual("$1.234.567,89", field.Result);
```

### Ver también

* class [FieldOptions](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
