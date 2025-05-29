---
title: DocumentBuilder.InsertStructuredDocumentTag
linktitle: InsertStructuredDocumentTag
articleTitle: InsertStructuredDocumentTag
second_title: Aspose.Words för .NET
description: Förbättra dina dokument enkelt med DocumentBuilder-metoden InsertStructuredDocumentTag. Lägg enkelt till strukturerade dokumenttaggar för bättre organisation!
type: docs
weight: 480
url: /sv/net/aspose.words/documentbuilder/insertstructureddocumenttag/
---
## DocumentBuilder.InsertStructuredDocumentTag method

Infogar en[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) in i dokumentet.

```csharp
public StructuredDocumentTag InsertStructuredDocumentTag(SdtType type)
```

### Returvärde

De[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) noden som just infogades.

## Exempel

Visar hur man enkelt infogar en strukturerad dokumenttagg.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveTo(doc.FirstSection.Body.Paragraphs[3]);
// Observera att endast följande StructuredDocumentTag-typer är tillåtna för infogning:
// SdtType.PlainText, SdtType.RichText, SdtType.Checkbox, SdtType.DropDownList,
// SdtType.ComboBox, SdtType.Bild, SdtType.Datum.
// Markeringsnivån för den infogade StructuredDocumentTag detekteras automatiskt och beror på vilken position den infogas på.
// Tillagd StructuredDocumentTag kommer att ärva stycke- och teckensnittsformatering från markörens position.
StructuredDocumentTag sdtPlain = builder.InsertStructuredDocumentTag(SdtType.PlainText);

doc.Save(ArtifactsDir + "StructuredDocumentTag.InsertStructuredDocumentTag.docx");
```

### Se även

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* enum [SdtType](../../../aspose.words.markup/sdttype/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
