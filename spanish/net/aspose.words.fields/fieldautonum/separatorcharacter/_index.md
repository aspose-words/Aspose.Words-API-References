---
title: FieldAutoNum.SeparatorCharacter
linktitle: SeparatorCharacter
articleTitle: SeparatorCharacter
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldAutoNum SeparatorCharacter, personalice fácilmente su carácter separador para mejorar el formato de los datos y facilitar su uso.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldautonum/separatorcharacter/
---
## FieldAutoNum.SeparatorCharacter property

Obtiene o establece el carácter separador que se utilizará.

```csharp
public string SeparatorCharacter { get; set; }
```

## Ejemplos

Muestra cómo numerar párrafos utilizando campos de numeración automática.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cada campo AUTONUM muestra el valor actual de un recuento continuo de campos AUTONUM,
// permitiéndonos numerar automáticamente elementos como una lista numerada.
//Este campo mostrará un número "1".
FieldAutoNum field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 1.");

Assert.AreEqual(" AUTONUM ", field.GetFieldCode());

field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 2.");

// El carácter separador, que aparece en el campo resultado inmediatamente después del número, es un punto por defecto.
// Si dejamos esta propiedad nula, nuestro segundo campo AUTONUM mostrará "2." en el documento.
Assert.IsNull(field.SeparatorCharacter);

//Podemos configurar esta propiedad para aplicar el primer carácter de su cadena como el nuevo carácter separador.
// En este caso, nuestro campo AUTONUM ahora mostrará "2:".
field.SeparatorCharacter = ":";

Assert.AreEqual(" AUTONUM  \\s :", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUM.docx");
```

### Ver también

* class [FieldAutoNum](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
