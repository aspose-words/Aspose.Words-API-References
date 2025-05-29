---
title: MailMergeRegionInfo.MustacheTags
linktitle: MustacheTags
articleTitle: MustacheTags
second_title: Aspose.Words para .NET
description: Descubra la propiedad MustacheTags de MailMergeRegionInfo, que devuelve de manera eficiente una lista completa de etiquetas Mustache secundarias para una integración de datos perfecta.
type: docs
weight: 50
url: /es/net/aspose.words.mailmerging/mailmergeregioninfo/mustachetags/
---
## MailMergeRegionInfo.MustacheTags property

Devuelve una lista de etiquetas "bigote" secundarias.

```csharp
public IList<MustacheTag> MustacheTags { get; }
```

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

* class [MustacheTag](../../mustachetag/)
* class [MailMergeRegionInfo](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)
