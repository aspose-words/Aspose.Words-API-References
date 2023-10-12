---
title: FieldAddressBlock.FormatAddressOnCountryOrRegion
second_title: Referencia de API de Aspose.Words para .NET
description: FieldAddressBlock propiedad. Obtiene o establece si se debe formatear la dirección según el país/región del destinatario según lo definido por POSTCODE Unión Postal Universal 2006.
type: docs
weight: 30
url: /es/net/aspose.words.fields/fieldaddressblock/formataddressoncountryorregion/
---
## FieldAddressBlock.FormatAddressOnCountryOrRegion property

Obtiene o establece si se debe formatear la dirección según el país/región del destinatario según lo definido por POST*CODE (Unión Postal Universal 2006).

```csharp
public bool FormatAddressOnCountryOrRegion { get; set; }
```

### Ejemplos

Muestra cómo insertar un campo ADDRESSBLOCK.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldAddressBlock field = (FieldAddressBlock)builder.InsertField(FieldType.FieldAddressBlock, true);

Assert.AreEqual(" ADDRESSBLOCK ", field.GetFieldCode());

// Establecer esto en "2" incluirá todos los países y regiones,
// a menos que sea el especificado en la propiedad ExcludedCountryOrRegionName.
field.IncludeCountryOrRegionName = "2";
field.FormatAddressOnCountryOrRegion = true;
field.ExcludedCountryOrRegionName = "United States";
field.NameAndAddressFormat = "<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>";

// De forma predeterminada, esta propiedad contendrá el ID de idioma del primer carácter del documento.
// Podemos establecer una cultura diferente para el campo para formatear el resultado de esta manera.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(
    " ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033",
    field.GetFieldCode());
```

### Ver también

* class [FieldAddressBlock](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldaddressblock/)
* asamblea [Aspose.Words](../../../)


