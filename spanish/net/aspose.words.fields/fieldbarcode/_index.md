---
title: FieldBarcode
second_title: Referencia de API de Aspose.Words para .NET
description: Implementa el campo BARCODE.
type: docs
weight: 1480
url: /es/net/aspose.words.fields/fieldbarcode/
---
## FieldBarcode class

Implementa el campo BARCODE.

```csharp
public class FieldBarcode : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldBarcode](fieldbarcode)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end) { get; } | Obtiene el nodo que representa el final del campo. |
| [FacingIdentificationMark](../../aspose.words.fields/fieldbarcode/facingidentificationmark) { get; set; } | Obtiene o establece el tipo de una Marca de identificación de frente (FIM) para insertar. |
| [Format](../../aspose.words.fields/field/format) { get; } | Obtiene un[`FieldFormat`](../fieldformat) objeto que proporciona acceso escrito al formato del campo. |
| [IsBookmark](../../aspose.words.fields/fieldbarcode/isbookmark) { get; set; } | Obtiene o establece si[`PostalAddress`](./postaladdress) es el nombre de un marcador. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [IsUSPostalAddress](../../aspose.words.fields/fieldbarcode/isuspostaladdress) { get; set; } | Obtiene o establece si[`PostalAddress`](./postaladdress) es una dirección postal de EE. UU. |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Obtiene o establece el LCID del campo. |
| [PostalAddress](../../aspose.words.fields/fieldbarcode/postaladdress) { get; set; } | Obtiene o establece la dirección postal utilizada para generar un código de barras o el nombre del marcador que hace referencia a él. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Obtiene el nodo que representa el separador de campos. Puede ser nulo. |
| [Start](../../aspose.words.fields/field/start) { get; } | Obtiene el nodo que representa el inicio del campo. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Obtiene el tipo de campo de Microsoft Word. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Se incluyen tanto el código de campo como el resultado de campo de los campos secundarios. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). |
| [Remove](../../aspose.words.fields/field/remove)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo principal, devuelve su párrafo principal. Si el campo ya está eliminado, devuelve **nulo** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Realiza el desvinculado del campo. |
| [Update](../../aspose.words.fields/field/update)() | Realiza la actualización del campo. Se lanza si el campo ya se está actualizando. |
| [Update](../../aspose.words.fields/field/update)(bool) | Realiza una actualización de campo. Se lanza si el campo ya se está actualizando. |

### Observaciones

Inserta un código de barras postal en una forma de dirección legible por máquina utilizada por el Servicio Postal de EE. UU.

### Ejemplos

Muestra cómo usar el campo CÓDIGO DE BARRAS para mostrar códigos postales de EE. UU. en forma de código de barras.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// A continuación se muestran dos formas de usar los campos de CÓDIGO DE BARRAS para mostrar valores personalizados como códigos de barras.
// 1 - Almacene el valor que mostrará el código de barras en la propiedad PostalAddress:
FieldBarcode field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);

// Este valor debe ser un código postal válido.
field.PostalAddress = "96801";
field.IsUSPostalAddress = true;
field.FacingIdentificationMark = "C";

Assert.AreEqual(" BARCODE  96801 \\u \\f C", field.GetFieldCode());

builder.InsertBreak(BreakType.LineBreak);

// 2 - Hacer referencia a un marcador que almacena el valor que mostrará este código de barras:
field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);
field.PostalAddress = "BarcodeBookmark";
field.IsBookmark = true;

Assert.AreEqual(" BARCODE  BarcodeBookmark \\b", field.GetFieldCode());

// El marcador al que hace referencia el campo BARCODE en su propiedad PostalAddress
// necesita contener nada más que el código postal válido.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("BarcodeBookmark");
builder.Writeln("968877");
builder.EndBookmark("BarcodeBookmark");

doc.Save(ArtifactsDir + "Field.BARCODE.docx");
```

### Ver también

* class [Field](../field)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
