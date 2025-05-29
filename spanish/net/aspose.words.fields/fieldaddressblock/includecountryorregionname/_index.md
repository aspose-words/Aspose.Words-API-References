---
title: FieldAddressBlock.IncludeCountryOrRegionName
linktitle: IncludeCountryOrRegionName
articleTitle: IncludeCountryOrRegionName
second_title: Aspose.Words para .NET
description: Descubra la propiedad IncludeCountryOrRegionName de FieldAddressBlock para administrar fácilmente la inclusión de nombres de países/regiones para un formato de dirección mejorado.
type: docs
weight: 40
url: /es/net/aspose.words.fields/fieldaddressblock/includecountryorregionname/
---
## FieldAddressBlock.IncludeCountryOrRegionName property

Obtiene o establece si se debe incluir el nombre del país/región.

```csharp
public string IncludeCountryOrRegionName { get; set; }
```

## Ejemplos

Muestra cómo insertar un campo ADDRESSBLOCK.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldAddressBlock field = (FieldAddressBlock)builder.InsertField(FieldType.FieldAddressBlock, true);

Assert.AreEqual(" ADDRESSBLOCK ", field.GetFieldCode());

// Si se establece en "2", se incluirán todos los países y regiones.
// a menos que sea el especificado en la propiedad ExcludedCountryOrRegionName.
field.IncludeCountryOrRegionName = "2";
field.FormatAddressOnCountryOrRegion = true;
field.ExcludedCountryOrRegionName = "United States";
field.NameAndAddressFormat = "<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>";

// De forma predeterminada, esta propiedad contendrá el ID de idioma del primer carácter del documento.
//Podemos establecer una cultura diferente para el campo para formatear el resultado de esta manera.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(
    " ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033",
    field.GetFieldCode());
```

### Ver también

* class [FieldAddressBlock](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
