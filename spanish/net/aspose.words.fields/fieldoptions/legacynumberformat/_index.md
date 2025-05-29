---
title: FieldOptions.LegacyNumberFormat
linktitle: LegacyNumberFormat
articleTitle: LegacyNumberFormat
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldOptions LegacyNumberFormat para habilitar o deshabilitar formatos de números heredados para los campos, mejorando la compatibilidad y el rendimiento.
type: docs
weight: 160
url: /es/net/aspose.words.fields/fieldoptions/legacynumberformat/
---
## FieldOptions.LegacyNumberFormat property

Obtiene o establece el valor que indica si el formato de número heredado (anterior a AW 13.10) para los campos está habilitado o no.

```csharp
public bool LegacyNumberFormat { get; set; }
```

## Observaciones

Cuando esta propiedad se establece en`verdadero`, el símbolo de plantilla "#" funcionó como en .net: Reemplaza el signo de almohadilla con el dígito correspondiente si hay uno presente; de lo contrario, no aparecen símbolos en la cadena de resultados.

Cuando esta propiedad se establece en`FALSO`El símbolo de plantilla "#" funciona como MS Word: Este elemento de formato especifica los dígitos necesarios que se mostrarán en el resultado. Si el resultado no incluye un dígito en ese lugar, MS Word muestra un espacio. Por ejemplo, { = 9 + 6 \# $### } muestra $ 15.

El valor predeterminado es`FALSO`.

## Ejemplos

Muestra cómo habilitar el formato de números heredados para los campos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("= 2 + 3 \\# $##");

Assert.AreEqual("$ 5", field.Result);

doc.FieldOptions.LegacyNumberFormat = true;
field.Update();

Assert.AreEqual("$5", field.Result);
```

### Ver también

* class [FieldOptions](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
