---
title: Document.ExtractPages
linktitle: ExtractPages
articleTitle: ExtractPages
second_title: Aspose.Words para .NET
description: Descubra el método Document ExtractPages para recuperar fácilmente rangos de páginas específicos, mejorando la gestión y la eficiencia de sus documentos.
type: docs
weight: 640
url: /es/net/aspose.words/document/extractpages/
---
## Document.ExtractPages method

Devuelve el[`Document`](../) objeto que representa un rango específico de páginas.

```csharp
public Document ExtractPages(int index, int count)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| index | Int32 | El índice basado en cero de la primera página a extraer. |
| count | Int32 | Número de páginas a extraer. |

## Observaciones

El documento resultante debe parecerse al de MS Word, como si hubiéramos realizado 'Imprimir páginas específicas': la numeración, los encabezados/pies de página y el diseño de tablas cruzadas se conservarán. Pero debido a una gran cantidad de matices que aparecen al reducir el número de páginas, la coincidencia completa del diseño es una tarea bastante complicada que requiere mucho esfuerzo. Dependiendo de la complejidad del documento, puede haber ligeras diferencias en el diseño del contenido del documento resultante en comparación con el documento original. Cualquier comentario será muy apreciado.

## Ejemplos

Muestra cómo obtener un rango específico de páginas del documento.

```csharp
Document doc = new Document(MyDir + "Layout entities.docx");

doc = doc.ExtractPages(0, 2);

doc.Save(ArtifactsDir + "Document.ExtractPages.docx");
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
