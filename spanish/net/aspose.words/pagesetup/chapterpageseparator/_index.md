---
title: PageSetup.ChapterPageSeparator
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: Aspose.Words para .NET
description: PageSetup ChapterPageSeparator propiedad. Obtiene o establece el carácter separador que aparece entre el número de capítulo y el número de página en C#.
type: docs
weight: 90
url: /es/net/aspose.words/pagesetup/chapterpageseparator/
---
## PageSetup.ChapterPageSeparator property

Obtiene o establece el carácter separador que aparece entre el número de capítulo y el número de página.

```csharp
public ChapterPageSeparator ChapterPageSeparator { get; set; }
```

## Observaciones

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

* enum [ChapterPageSeparator](../../chapterpageseparator/)
* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
