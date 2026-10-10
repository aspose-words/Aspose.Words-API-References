---
title: "Enumeración Aspose::Words::Layout::LayoutEntityType"
linktitle: "LayoutEntityType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Enumeración Aspose::Words::Layout::LayoutEntityType. Tipos de las entidades de diseño en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.layout/layoutentitytype/
---
## LayoutEntityType enum


Tipos de las entidades de diseño.

```cpp
enum class LayoutEntityType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | n/a | Valor predeterminado. |
| Page | n/a | Representa una página de un documento. La página puede tener entidades hijas [Column](./), [HeaderFooter](./) y [Comment](./). |
| Column | n/a | Representa una columna de texto en una página. La columna puede tener las mismas entidades hijas que [Cell](./), además de entidades [Footnote](./), [Endnote](./) y [NoteSeparator](./). |
| Row | n/a | Representa una fila de tabla. La fila puede tener [Cell](./) como entidades hijas. |
| Cell | n/a | Representa una celda de tabla. La celda puede tener entidades hijas [Line](./) y [Row](./). |
| Line | n/a | Representa una línea de caracteres de texto y objetos en línea. La línea puede tener entidades hijas [Span](./). |
| Span | n/a | Representa uno o más caracteres en una línea. Esto incluye caracteres especiales como marcadores de inicio/fin de campo, marcadores y comentarios. Span no puede tener entidades secundarias. |
| Footnote | n/a | Representa un marcador de posición para el contenido de la nota al pie. Footnote puede tener entidades secundarias [Note](./). |
| Endnote | n/a | Representa un marcador de posición para el contenido de la nota final. Endnote puede tener entidades secundarias [Note](./). |
| Note | n/a | Representa un marcador de posición para el contenido de la nota. Note puede tener entidades secundarias [Line](./) y [Row](./). |
| HeaderFooter | n/a | Representa un marcador de posición para el contenido de encabezado/pie de página en una página. [HeaderFooter](../../aspose.words/headerfooter/) puede tener entidades secundarias [Line](./) y [Row](./). |
| TextBox | n/a | Representa el área de texto dentro de una forma. Textbox puede tener entidades secundarias [Line](./) y [Row](./). |
| Comment | n/a | Representa un marcador de posición para el contenido del comentario. [Comment](../../aspose.words/comment/) puede tener entidades secundarias [Line](./) y [Row](./). |
| NoteSeparator | n/a | Representa el separador de nota al pie/nota final. NoteSeparator puede tener entidades secundarias [Line](./) y [Row](./). |

## Ver también

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
