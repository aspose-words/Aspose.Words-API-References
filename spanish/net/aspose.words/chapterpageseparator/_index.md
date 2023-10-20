---
title: ChapterPageSeparator Enum
linktitle: ChapterPageSeparator
articleTitle: ChapterPageSeparator
second_title: Aspose.Words para .NET
description: Aspose.Words.ChapterPageSeparator enumeración. Define el carácter separador que aparece entre el capítulo y el número de página en C#.
type: docs
weight: 200
url: /es/net/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enumeration

Define el carácter separador que aparece entre el capítulo y el número de página.

```csharp
public enum ChapterPageSeparator
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Hyphen | `0` | Dos puntos. |
| Period | `1` | Un punto. |
| Colon | `2` | Dos puntos. |
| EmDash | `3` | Un guión enfatizado. |
| EnDash | `4` | Un guión estándar. |

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

* class [PageSetup](../pagesetup/)
* property [ChapterPageSeparator](../pagesetup/chapterpageseparator/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
