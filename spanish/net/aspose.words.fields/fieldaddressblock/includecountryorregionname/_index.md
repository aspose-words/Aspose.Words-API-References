---
title: FieldAddressBlock.IncludeCountryOrRegionName
second_title: Referencia de API de Aspose.Words para .NET
description: FieldAddressBlock propiedad. Obtiene o establece si incluir el nombre del país/región.
type: docs
weight: 40
url: /es/net/aspose.words.fields/fieldaddressblock/includecountryorregionname/
---
## FieldAddressBlock.IncludeCountryOrRegionName property

Obtiene o establece si incluir el nombre del país/región.

```csharp
public string IncludeCountryOrRegionName { get; set; }
```

### Ejemplos

Muestra cómo insertar un campo DIRECCIÓN.

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
// Podemos establecer una cultura diferente para que el campo formatee el resultado de esta manera.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(
    " ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033",
    field.GetFieldCode());
```

### Ver también

* class [FieldAddressBlock](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldaddressblock/)
* asamblea [Aspose.Words](../../../)


