---
title: FieldAddressBlock
second_title: Referencia de API de Aspose.Words para .NET
description: Implementa el campo DIRECCIÓN BLOQUE.
type: docs
weight: 1380
url: /es/net/aspose.words.fields/fieldaddressblock/
---
## FieldAddressBlock class

Implementa el campo DIRECCIÓN BLOQUE.

```csharp
public class FieldAddressBlock : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldAddressBlock](fieldaddressblock)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end) { get; } | Obtiene el nodo que representa el final del campo. |
| [ExcludedCountryOrRegionName](../../aspose.words.fields/fieldaddressblock/excludedcountryorregionname) { get; set; } | Obtiene o establece el nombre del país/región excluido. |
| [Format](../../aspose.words.fields/field/format) { get; } | Obtiene un[`FieldFormat`](../fieldformat) objeto que proporciona acceso escrito al formato del campo. |
| [FormatAddressOnCountryOrRegion](../../aspose.words.fields/fieldaddressblock/formataddressoncountryorregion) { get; set; } | Obtiene o establece si formatear la dirección de acuerdo con el país/región del destinatario según lo definido por POST*CODE (Universal Postal Union 2006). |
| [IncludeCountryOrRegionName](../../aspose.words.fields/fieldaddressblock/includecountryorregionname) { get; set; } | Obtiene o establece si incluir el nombre del país/región. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LanguageId](../../aspose.words.fields/fieldaddressblock/languageid) { get; set; } | Obtiene o establece el ID de idioma utilizado para formatear la dirección. |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Obtiene o establece el LCID del campo. |
| [NameAndAddressFormat](../../aspose.words.fields/fieldaddressblock/nameandaddressformat) { get; set; } | Obtiene o establece el formato de nombre y dirección. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Obtiene el nodo que representa el separador de campos. Puede ser nulo. |
| [Start](../../aspose.words.fields/field/start) { get; } | Obtiene el nodo que representa el inicio del campo. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Obtiene el tipo de campo de Microsoft Word. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Se incluyen tanto el código de campo como el resultado de campo de los campos secundarios. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). |
| [GetFieldNames](../../aspose.words.fields/fieldaddressblock/getfieldnames)() | Devuelve una colección de nombres de campos de combinación de correspondencia usados por el campo. |
| [Remove](../../aspose.words.fields/field/remove)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo principal, devuelve su párrafo principal. Si el campo ya está eliminado, devuelve **nulo** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Realiza el desvinculado del campo. |
| [Update](../../aspose.words.fields/field/update)() | Realiza la actualización del campo. Se lanza si el campo ya se está actualizando. |
| [Update](../../aspose.words.fields/field/update)(bool) | Realiza una actualización de campo. Se lanza si el campo ya se está actualizando. |

### Observaciones

Representa un bloque de direcciones. Unbloque de direcciones es un bloque de texto que especifica información apropiada para una dirección postal, en el orden requerido por el país de destino.

### Ejemplos

Muestra cómo obtener nombres de campos de combinación de correspondencia utilizados por un campo.

```csharp
Document doc = new Document(MyDir + "Field sample - ADDRESSBLOCK.docx");

string[] addressFieldsExpect =
{
    "Company", "First Name", "Middle Name", "Last Name", "Suffix", "Address 1", "City", "State",
    "Country or Region", "Postal Code"
};

FieldAddressBlock addressBlockField = (FieldAddressBlock) doc.Range.Fields[0];
string[] addressBlockFieldNames = addressBlockField.GetFieldNames();
```

### Ver también

* class [Field](../field)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
