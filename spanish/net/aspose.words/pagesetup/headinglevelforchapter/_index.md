---
title: PageSetup.HeadingLevelForChapter
linktitle: HeadingLevelForChapter
articleTitle: HeadingLevelForChapter
second_title: Aspose.Words para .NET
description: PageSetup HeadingLevelForChapter propiedad. Obtiene o establece el estilo de nivel de encabezado que se aplica a los títulos de los capítulos en el documento en C#.
type: docs
weight: 180
url: /es/net/aspose.words/pagesetup/headinglevelforchapter/
---
## PageSetup.HeadingLevelForChapter property

Obtiene o establece el estilo de nivel de encabezado que se aplica a los títulos de los capítulos en el documento.

```csharp
public int HeadingLevelForChapter { get; set; }
```

## Observaciones

Puede ser un número del 0 al 9. 0 significa que no hay número de capítulo si se aplica al número de página.

Antes de poder crear números de página que incluyan números de capítulo, los encabezados del documento deben tener aplicado un formato de esquema numerado.

## Ejemplos

Muestra cómo trabajar con capítulos de página.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

PageSetup pageSetup = doc.FirstSection.PageSetup;

pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;
pageSetup.ChapterPageSeparator = Aspose.Words.ChapterPageSeparator.Colon;
pageSetup.HeadingLevelForChapter = 1;
```

### Ver también

* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
