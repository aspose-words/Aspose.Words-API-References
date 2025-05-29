---
title: XmlDataSource
linktitle: XmlDataSource
articleTitle: XmlDataSource
second_title: Aspose.Words för .NET
description: Skapa enkelt en kraftfull datakälla med XmlDataSource-konstruktorn och läs in XML-data med optimerade standardalternativ för sömlös integration.
type: docs
weight: 10
url: /sv/net/aspose.words.reporting/xmldatasource/xmldatasource/
---
## XmlDataSource(*string*) {#constructor_4}

Skapar en ny datakälla med data från en XML-fil med standardalternativ för inläsning av XML-data.

```csharp
public XmlDataSource(string xmlPath)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| xmlPath | String | Sökvägen till XML-filen som ska användas som datakälla. |

## Exempel

Visa hur man använder XML som datakälla (sträng).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

XmlDataSource dataSource = new XmlDataSource(MyDir + "List of people.xml");
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataString.docx");
```

### Se även

* class [XmlDataSource](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)

---

## XmlDataSource(*Stream*) {#constructor}

Skapar en ny datakälla med data från en XML-ström med standardalternativ för inläsning av XML-data.

```csharp
public XmlDataSource(Stream xmlStream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| xmlStream | Stream | Den XML-dataström som ska användas som datakälla. |

## Exempel

Visa hur man använder XML som datakälla (ström).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

using (FileStream stream = File.OpenRead(MyDir + "List of people.xml"))
{
    XmlDataSource dataSource = new XmlDataSource(stream);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataStream.docx");
```

### Se även

* class [XmlDataSource](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)

---

## XmlDataSource(*string, string*) {#constructor_6}

Skapar en ny datakälla med data från en XML-fil med hjälp av en XML-schemadefinitionsfil. Standardalternativen används för inläsning av XML-data.

```csharp
public XmlDataSource(string xmlPath, string xmlSchemaPath)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| xmlPath | String | Sökvägen till XML-filen som ska användas som datakälla. |
| xmlSchemaPath | String | Sökvägen till XML-schemadefinitionsfilen som tillhandahåller schemat för XML -filen. |

### Se även

* class [XmlDataSource](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, Stream*) {#constructor_2}

Skapar en ny datakälla med data från en XML-ström med hjälp av en XML Schema Definition-ström. Standardalternativen används för inläsning av XML-data.

```csharp
public XmlDataSource(Stream xmlStream, Stream xmlSchemaStream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| xmlStream | Stream | Den XML-dataström som ska användas som datakälla. |
| xmlSchemaStream | Stream | Flödet av XML-schemadefinition som tillhandahåller schemat för XML-data. |

### Se även

* class [XmlDataSource](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)

---

## XmlDataSource(*string, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_5}

Skapar en ny datakälla med data från en XML-fil med hjälp av de angivna alternativen för inläsning av XML-data.

```csharp
public XmlDataSource(string xmlPath, XmlDataLoadOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| xmlPath | String | Sökvägen till XML-filen som ska användas som datakälla. |
| options | XmlDataLoadOptions | Alternativ för inläsning av XML-data. |

### Se även

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_1}

Skapar en ny datakälla med data från en XML-ström med hjälp av de angivna alternativen för XML-datainläsning.

```csharp
public XmlDataSource(Stream xmlStream, XmlDataLoadOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| xmlStream | Stream | Den XML-dataström som ska användas som datakälla. |
| options | XmlDataLoadOptions | Alternativ för inläsning av XML-data. |

### Se även

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)

---

## XmlDataSource(*string, string, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_7}

Skapar en ny datakälla med data från en XML-fil med hjälp av en XML-schemadefinitionsfil. De angivna -alternativen används för inläsning av XML-data.

```csharp
public XmlDataSource(string xmlPath, string xmlSchemaPath, XmlDataLoadOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| xmlPath | String | Sökvägen till XML-filen som ska användas som datakälla. |
| xmlSchemaPath | String | Sökvägen till XML-schemadefinitionsfilen som tillhandahåller schemat för XML -filen. |
| options | XmlDataLoadOptions | Alternativ för inläsning av XML-data. |

### Se även

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, Stream, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_3}

Skapar en ny datakälla med data från en XML-ström med hjälp av en XML Schema Definition-ström. De angivna -alternativen används för inläsning av XML-data.

```csharp
public XmlDataSource(Stream xmlStream, Stream xmlSchemaStream, XmlDataLoadOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| xmlStream | Stream | Den XML-dataström som ska användas som datakälla. |
| xmlSchemaStream | Stream | Flödet av XML-schemadefinition som tillhandahåller schemat för XML-data. |
| options | XmlDataLoadOptions | Alternativ för inläsning av XML-data. |

### Se även

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* namnutrymme [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* hopsättning [Aspose.Words](../../../)
