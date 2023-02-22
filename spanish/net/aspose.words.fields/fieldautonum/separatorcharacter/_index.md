---
title: FieldAutoNum.SeparatorCharacter
second_title: Referencia de API de Aspose.Words para .NET
description: FieldAutoNum propiedad. Obtiene o establece el carácter separador que se utilizará.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldautonum/separatorcharacter/
---
## FieldAutoNum.SeparatorCharacter property

Obtiene o establece el carácter separador que se utilizará.

```csharp
public string SeparatorCharacter { get; set; }
```

### Ejemplos

Muestra cómo numerar párrafos usando campos de numeración automática.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cada campo AUTONUM muestra el valor actual de un conteo continuo de campos AUTONUM,
// permitiéndonos numerar elementos automáticamente como una lista numerada.
// Este campo mostrará un número "1.".
FieldAutoNum field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 1.");

Assert.AreEqual(" AUTONUM ", field.GetFieldCode());

field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 2.");

// El carácter separador, que aparece en el resultado del campo inmediatamente después del número, es un punto por defecto.
// Si dejamos esta propiedad nula, nuestro segundo campo AUTONUM mostrará "2". en el documento
Assert.IsNull(field.SeparatorCharacter);

// Podemos establecer esta propiedad para aplicar el primer carácter de su cadena como el nuevo carácter separador.
// En este caso, nuestro campo AUTONUM ahora mostrará "2:".
field.SeparatorCharacter = ":";

Assert.AreEqual(" AUTONUM  \\s :", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUM.docx");
```

### Ver también

* class [FieldAutoNum](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldautonum/)
* asamblea [Aspose.Words](../../../)


