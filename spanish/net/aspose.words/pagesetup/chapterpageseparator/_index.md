---
title: PageSetup.ChapterPageSeparator
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChapterPageSeparator en PageSetup. Personalice fácilmente el carácter separador entre los números de capítulo y página para una apariencia impecable.
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

Antes de poder crear números de página que incluyan números de capítulo, es necesario aplicar un formato de esquema numerado a los encabezados del documento.

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
