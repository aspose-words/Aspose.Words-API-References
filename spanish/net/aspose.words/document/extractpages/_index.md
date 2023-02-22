---
title: Document.ExtractPages
second_title: Referencia de API de Aspose.Words para .NET
description: Document método. Devuelve elDocument objeto que representa el rango especificado de páginas.
type: docs
weight: 580
url: /es/net/aspose.words/document/extractpages/
---
## Document.ExtractPages method

Devuelve el[`Document`](../) objeto que representa el rango especificado de páginas.

```csharp
public Document ExtractPages(int index, int count)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| index | Int32 | El índice de base cero de la primera página que se va a extraer. |
| count | Int32 | Número de páginas a extraer. |

### Observaciones

El documento resultante debe verse como el de MS Word, como si hubiéramos realizado 'Imprimir páginas específicas': la numeración, encabezados/pies de página y el diseño de tablas cruzadas se mantendrán. Pero debido a una gran cantidad de matices, que aparecen mientras se reduce el número de páginas, la coincidencia completa del diseño es una tarea complicada y silenciosa que requiere mucho esfuerzo. Dependiendo de la complejidad del documento, puede haber ligeras diferencias en el diseño del contenido del documento resultante en comparación con el documento de origen. Cualquier comentario sería ser muy apreciado.

### Ejemplos

Muestra cómo obtener un rango específico de páginas del documento.

```csharp
Document doc = new Document(MyDir + "Layout entities.docx");

doc = doc.ExtractPages(0, 2);

doc.Save(ArtifactsDir + "Document.ExtractPages.docx");
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)


