---
title: List.IsRestartAtEachSection
second_title: Referencia de API de Aspose.Words para .NET
description: List propiedad. Especifica si la lista debe reiniciarse en cada sección. El valor predeterminado es falso .
type: docs
weight: 50
url: /es/net/aspose.words.lists/list/isrestartateachsection/
---
## List.IsRestartAtEachSection property

Especifica si la lista debe reiniciarse en cada sección. El valor predeterminado es **falso** .

```csharp
public bool IsRestartAtEachSection { get; set; }
```

### Observaciones

Esta opción solo se admite en los formatos de documento RTF, DOC y DOCX.

Esta opción se escribirá en DOCX solo si[`OoxmlCompliance`](../../../aspose.words.saving/ooxmlcompliance/) es mas alto entoncesEcma376_2006.

### Ejemplos

Muestra cómo configurar una lista para reiniciar la numeración en cada sección.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

doc.Lists.Add(ListTemplate.NumberDefault);

Aspose.Words.Lists.List list = doc.Lists[0];
list.IsRestartAtEachSection = restartListAtEachSection;

// La propiedad "IsRestartAtEachSection" solo será aplicable cuando
// el nivel de cumplimiento de OOXML del documento corresponde a un estándar más nuevo que "OoxmlComplianceCore.Ecma376".
OoxmlSaveOptions options = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Transitional
};

builder.ListFormat.List = list;

builder.Writeln("List item 1");
builder.Writeln("List item 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("List item 3");
builder.Writeln("List item 4");

doc.Save(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx");

Assert.AreEqual(restartListAtEachSection, doc.Lists[0].IsRestartAtEachSection);
```

### Ver también

* class [List](../)
* espacio de nombres [Aspose.Words.Lists](../../list/)
* asamblea [Aspose.Words](../../../)


