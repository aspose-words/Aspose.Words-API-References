---
title: Class FieldSymbol
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fields.FieldSymbol clase. Implementa un campo SÍMBOLO.
type: docs
weight: 2460
url: /es/net/aspose.words.fields/fieldsymbol/
---
## FieldSymbol class

Implementa un campo SÍMBOLO.

Para obtener más información, visite el[Trabajar con campos](https://docs.aspose.com/words/net/working-with-fields/) artículo de documentación.

```csharp
public class FieldSymbol : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldSymbol](fieldsymbol/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CharacterCode](../../aspose.words.fields/fieldsymbol/charactercode/) { get; set; } | Obtiene o establece el valor del punto de código del carácter en decimal o hexadecimal. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [DontAffectsLineSpacing](../../aspose.words.fields/fieldsymbol/dontaffectslinespacing/) { get; set; } | Obtiene o establece si el carácter recuperado por el campo afecta el interlineado del párrafo. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [FontName](../../aspose.words.fields/fieldsymbol/fontname/) { get; set; } | Obtiene o establece el nombre de la fuente del carácter recuperado por el campo. |
| [FontSize](../../aspose.words.fields/fieldsymbol/fontsize/) { get; set; } | Obtiene o establece el tamaño en puntos de la fuente del carácter recuperado por el campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/) objeto que proporciona acceso escrito al formato del campo. |
| [IsAnsi](../../aspose.words.fields/fieldsymbol/isansi/) { get; set; } | Obtiene o establece si el código de carácter se interpreta como el valor de un carácter ANSI. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe volver a calcular su resultado). |
| [IsShiftJis](../../aspose.words.fields/fieldsymbol/isshiftjis/) { get; set; } | Obtiene o establece si el código de carácter se interpreta como el valor de un carácter SHIFT-JIS. |
| [IsUnicode](../../aspose.words.fields/fieldsymbol/isunicode/) { get; set; } | Obtiene o establece si el código de carácter se interpreta como el valor de un carácter Unicode. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campos. Puede ser`nulo` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtiene el nodo que representa el inicio del campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtiene el tipo de campo de Microsoft Word. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Devuelve texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Se incluyen tanto el código de campo como el resultado del campo de los campos secundarios. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Devuelve texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). |
| [Remove](../../aspose.words.fields/field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo principal, devuelve su párrafo principal. Si el campo ya está eliminado, devuelve`nulo` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Realiza la desvinculación del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Realiza la actualización del campo. Se produce si el campo ya se está actualizando. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Realiza una actualización de campo. Se produce si el campo ya se está actualizando. |

### Observaciones

Recupera el carácter cuyo valor de punto de código se especifica en decimal o hexadecimal.

### Ejemplos

Muestra cómo utilizar el campo SÍMBOLO.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A continuación se muestran tres formas de utilizar un campo SÍMBOLO para mostrar un solo carácter.
// 1 - Agregue un campo SÍMBOLO que muestre el símbolo © (Copyright), especificado por un código de carácter ANSI:
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// El código de carácter ANSI "U+00A9", o "169" en formato entero, está reservado para el símbolo de copyright.
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.AreEqual(" SYMBOL  169 \\a", field.GetFieldCode());

builder.Writeln(" Line 1");

// 2 - Agrega un campo SÍMBOLO que muestra el símbolo ∞ (Infinito) y modifica su apariencia:
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// En Unicode, el símbolo de infinito ocupa el código "221E".
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// Cambia la fuente de nuestro símbolo después de usar el Mapa de Caracteres de Windows
// para garantizar que la fuente pueda representar ese símbolo.
field.FontName = "Calibri";
field.FontSize = "24";

// Podemos configurar esta bandera para símbolos altos para que no empujen hacia abajo el resto del texto en su línea.
field.DontAffectsLineSpacing = true;

Assert.AreEqual(" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field.GetFieldCode());

builder.Writeln("Line 2");

// 3 - Agrega un campo SÍMBOLO que muestra el carácter あ,
// con una fuente que admita la página de códigos Shift-JIS (Windows-932):
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);
field.FontName = "MS Gothic";
field.CharacterCode = 0x82A0.ToString();
field.IsShiftJis = true;

Assert.AreEqual(" SYMBOL  33440 \\f \"MS Gothic\" \\j", field.GetFieldCode());

builder.Write("Line 3");

doc.Save(ArtifactsDir + "Field.SYMBOL.docx");
```

### Ver también

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)


