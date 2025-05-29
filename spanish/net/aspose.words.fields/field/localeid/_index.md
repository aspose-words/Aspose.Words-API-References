---
title: Field.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: Aspose.Words para .NET
description: Administre fácilmente la propiedad LocaleId de su campo. Obtenga o configure el LCID para mejorar la localización y la experiencia de usuario en sus aplicaciones.
type: docs
weight: 60
url: /es/net/aspose.words.fields/field/localeid/
---
## Field.LocaleId property

Obtiene o establece el LCID del campo.

```csharp
public int LocaleId { get; set; }
```

## Ejemplos

Muestra cómo insertar un campo y trabajar con su configuración regional.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte un campo FECHA y luego imprima la fecha que se mostrará.
//La cultura actual de tu hilo determina el formato de la fecha.
Field field = builder.InsertField(@"DATE");
Console.WriteLine($"Today's date, as displayed in the \"{CultureInfo.CurrentCulture.EnglishName}\" culture: {field.Result}");

Assert.AreEqual(1033, field.LocaleId);
//Cambiar la cultura de nuestro hilo afectará el resultado del campo FECHA.
// Otra forma de hacer que el campo FECHA muestre una fecha en una cultura diferente es utilizar su propiedad LocaleId.
// De esta manera podemos evitar cambiar la cultura del hilo para obtener este efecto.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
CultureInfo de = new CultureInfo("de-DE");
field.LocaleId = de.LCID;
field.Update();

Console.WriteLine($"Today's date, as displayed according to the \"{CultureInfo.GetCultureInfo(field.LocaleId).EnglishName}\" culture: {field.Result}");
```

### Ver también

* class [Field](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
