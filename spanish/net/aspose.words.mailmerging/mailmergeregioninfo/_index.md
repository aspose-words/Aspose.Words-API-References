---
title: MailMergeRegionInfo Class
linktitle: MailMergeRegionInfo
articleTitle: MailMergeRegionInfo
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.MailMerging.MailMergeRegionInfo para una gestión eficiente de la combinación de correspondencia. ¡Desbloquee la automatización fluida de documentos hoy mismo!
type: docs
weight: 4550
url: /es/net/aspose.words.mailmerging/mailmergeregioninfo/
---
## MailMergeRegionInfo class

Contiene información sobre una región de combinación de correspondencia.

Para obtener más información, visite el[Combinación de correspondencia e informes](https://docs.aspose.com/words/net/mail-merge-and-reporting/) Artículo de documentación.

```csharp
public class MailMergeRegionInfo
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [EndField](../../aspose.words.mailmerging/mailmergeregioninfo/endfield/) { get; } | Devuelve un campo final para la región. |
| [EndMustacheTag](../../aspose.words.mailmerging/mailmergeregioninfo/endmustachetag/) { get; } | Devuelve una etiqueta "bigote" final para la región. |
| [Fields](../../aspose.words.mailmerging/mailmergeregioninfo/fields/) { get; } | Devuelve una lista de campos secundarios. |
| [Level](../../aspose.words.mailmerging/mailmergeregioninfo/level/) { get; } | Devuelve el nivel de anidamiento de la región. |
| [MustacheTags](../../aspose.words.mailmerging/mailmergeregioninfo/mustachetags/) { get; } | Devuelve una lista de etiquetas "bigote" secundarias. |
| [Name](../../aspose.words.mailmerging/mailmergeregioninfo/name/) { get; } | Devuelve el nombre de la región. |
| [ParentRegion](../../aspose.words.mailmerging/mailmergeregioninfo/parentregion/) { get; } | Devuelve información de la región principal (nulo para la región de nivel superior). |
| [Regions](../../aspose.words.mailmerging/mailmergeregioninfo/regions/) { get; } | Devuelve una lista de regiones secundarias. |
| [StartField](../../aspose.words.mailmerging/mailmergeregioninfo/startfield/) { get; } | Devuelve un campo de inicio para la región. |
| [StartMustacheTag](../../aspose.words.mailmerging/mailmergeregioninfo/startmustachetag/) { get; } | Devuelve una etiqueta de inicio "bigote" para la región. |

## Ejemplos

Muestra cómo verificar las regiones de combinación de correspondencia.

```csharp
Document doc = new Document(MyDir + "Mail merge regions.docx");

// Devuelve una jerarquía completa de regiones de fusión que contienen MERGEFIELDs disponibles en el documento.
MailMergeRegionInfo regionInfo = doc.MailMerge.GetRegionsHierarchy();

// Obtener las regiones principales del documento.
IList<MailMergeRegionInfo> topRegions = regionInfo.Regions;

Assert.AreEqual(2, topRegions.Count);
Assert.AreEqual("Region1", topRegions[0].Name);
Assert.AreEqual("Region2", topRegions[1].Name);
Assert.AreEqual(1, topRegions[0].Level);
Assert.AreEqual(1, topRegions[1].Level);

// Obtener la región anidada en la primera región superior.
IList<MailMergeRegionInfo> nestedRegions = topRegions[0].Regions;

Assert.AreEqual(2, nestedRegions.Count);
Assert.AreEqual("NestedRegion1", nestedRegions[0].Name);
Assert.AreEqual("NestedRegion2", nestedRegions[1].Name);
Assert.AreEqual(2, nestedRegions[0].Level);
Assert.AreEqual(2, nestedRegions[1].Level);
Assert.AreEqual(0, nestedRegions[1].MustacheTags.Count);

// Obtener la lista de campos dentro de la primera región superior.
IList<Field> fieldList = topRegions[0].Fields;

Assert.AreEqual(4, fieldList.Count);

FieldMergeField startFieldMergeField = nestedRegions[0].StartField;

Assert.AreEqual("TableStart:NestedRegion1", startFieldMergeField.FieldName);

FieldMergeField endFieldMergeField = nestedRegions[0].EndField;

Assert.AreEqual("TableEnd:NestedRegion1", endFieldMergeField.FieldName);
```

### Ver también

* espacio de nombres [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../)
