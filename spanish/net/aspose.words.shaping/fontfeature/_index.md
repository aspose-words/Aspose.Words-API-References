---
title: FontFeature Enum
linktitle: FontFeature
articleTitle: FontFeature
second_title: Aspose.Words para .NET
description: Descubre la enumeración Aspose.Words.Shaping.FontFeature, que detalla el uso de glifos en fuentes para la representación de scripts. ¡Mejora tus conocimientos de tipografía hoy mismo!
type: docs
weight: 6860
url: /es/net/aspose.words.shaping/fontfeature/
---
## FontFeature enumeration

Las características proporcionan información sobre cómo se utilizan los glifos en una fuente para representar una escritura. https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags

```csharp
public enum FontFeature
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| GlyphCompositionDecomposition | `1667460464` | Para minimizar la cantidad de alternativas de glifos, a veces es deseable descomponer el glifo predeterminado para un carácter en dos o más glifos. Además, puede ser preferible componer glifos predeterminados para dos o más caracteres en un solo glifo para un mejor procesamiento de glifos. Esta característica permite dicha composición/descomposición. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#ccmp Etiqueta OpenType equivalente: 'ccmp' |
| StandardLigatures | `1818847073` | Reemplaza una secuencia de glifos con un solo glifo que se prefiere para fines tipográficos. Esta característica cubre las ligaduras que el diseñador/fabricante considera que se deben utilizar en condiciones normales. Etiqueta OpenType equivalente: 'liga' https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#liga |
| RequiredLigatures | `1919707495` | Reemplaza una secuencia de glifos con un solo glifo que se prefiere para fines tipográficos. Esta característica cubre aquellas ligaduras que el script determina como necesarias para su uso en condiciones normales. Esta característica es importante para algunos scripts para garantizar la correcta formación de glifos. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#rlig Etiqueta OpenType equivalente: 'rlig' |
| ContextualLigatures | `1668049255` | Reemplaza una secuencia de glifos con un solo glifo que se prefiere para fines tipográficos. A diferencia de otras características de ligadura, 'clig' especifica el contexto en el que se recomienda la ligadura. Esta capacidad es importante en algunos diseños de escritura y para ligaduras floreadas. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#clig Etiqueta OpenType equivalente: 'clig' |
| DiscretionaryLigatures | `1684826471` | Reemplaza una secuencia de glifos con un solo glifo que se prefiere para fines tipográficos. Esta característica cubre aquellas ligaduras que se pueden usar para efectos especiales, según preferencia del usuario. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#dlig Etiqueta OpenType equivalente: 'dlig' |
| HistoricalLigatures | `1751935335` | Algunas ligaduras eran de uso común en el pasado, pero hoy parecen anacrónicas. Algunas fuentes incluyen las formas históricas como alternativas, por lo que se pueden usar para un efecto de "período". Esta función reemplaza las formas predeterminadas (actuales) con las alternativas históricas. https://docs.microsoft.com/en-us/typography/opentype/spec/features_fj#hlig Etiqueta OpenType equivalente: 'hlig' |
| ProportionalFigures | `1886287213` | Reemplaza los glifos de figuras establecidos en anchos uniformes (tabulares) con los glifos correspondientes establecidos en anchos específicos del glifo (proporcionales). https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-pnum Etiqueta OpenType equivalente: 'pnum' |
| TabularFigures | `1953396077` | Reemplaza los glifos de figuras establecidos en anchos proporcionales con los glifos correspondientes establecidos en anchos uniformes (tabulares). Los anchos tabulares generalmente serán los predeterminados, pero no se puede asumir con seguridad. Por supuesto, esta característica no estaría presente en diseños monoespaciados. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-tnum Etiqueta OpenType equivalente: 'tnum' |
| LiningFigures | `1819178349` | Esta función cambia las figuras no alineadas seleccionadas a figuras alineadas. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#lnum Etiqueta OpenType equivalente: 'lnum' |
| OldstyleFigures | `1869509997` | Esta función cambia las figuras seleccionadas del estilo predeterminado o de línea al formato antiguo. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#onum Etiqueta OpenType equivalente: 'onum' |
| VerticalAlternates | `1986359924` | Transforma los glifos predeterminados en glifos apropiados para la presentación vertical en modo de escritura vertical. https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vert Etiqueta OpenType equivalente: 'vert' |
| VerticalAlternatesAndRotation | `1987212338` | Reemplaza algunos glifos de ancho fijo (medio, tercio o cuarto de ancho) o de ancho proporcional (principalmente latín o katakana) con formas adecuadas para escritura vertical (es decir, rotadas 90 grados en el sentido de las agujas del reloj). https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vrt2 Etiqueta OpenType equivalente: 'vrt2' |
| StylisticSet01 | `1936928817` | Conjunto estilístico 1 Además de, o en lugar de, alternativas estilísticas de glifos individuales (ver característica 'sal'), algunas fuentes pueden contener conjuntos de glifos variantes estilísticas correspondientes a partes del conjunto de caracteres, por ejemplo, múltiples variantes para letras minúsculas en una fuente latina. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-ss01---ss20 Etiqueta OpenType equivalente: 'ss01' |
| StylisticSet02 | `1936928818` | Conjunto estilístico 2 Etiqueta OpenType equivalente: 'ss02' |
| StylisticSet03 | `1936928819` | Conjunto estilístico 3 Etiqueta OpenType equivalente: 'ss03' |
| StylisticSet04 | `1936928820` | Conjunto estilístico 4 Etiqueta OpenType equivalente: 'ss04' |
| StylisticSet05 | `1936928821` | Conjunto estilístico 5 Etiqueta OpenType equivalente: 'ss05' |
| StylisticSet06 | `1936928822` | Conjunto estilístico 6 Etiqueta OpenType equivalente: 'ss06' |
| StylisticSet07 | `1936928823` | Conjunto estilístico 7 Etiqueta OpenType equivalente: 'ss07' |
| StylisticSet08 | `1936928824` | Conjunto estilístico 8 Etiqueta OpenType equivalente: 'ss08' |
| StylisticSet09 | `1936928825` | Conjunto estilístico 9 Etiqueta OpenType equivalente: 'ss09' |
| StylisticSet10 | `1936929072` | Conjunto estilístico 10 Etiqueta OpenType equivalente: 'ss10' |
| StylisticSet11 | `1936929073` | Conjunto estilístico 11 Etiqueta OpenType equivalente: 'ss11' |
| StylisticSet12 | `1936929074` | Conjunto estilístico 12 Etiqueta OpenType equivalente: 'ss12' |
| StylisticSet13 | `1936929075` | Conjunto estilístico 13 Etiqueta OpenType equivalente: 'ss13' |
| StylisticSet14 | `1936929076` | Conjunto estilístico 14 Etiqueta OpenType equivalente: 'ss14' |
| StylisticSet15 | `1936929077` | Conjunto estilístico 15 Etiqueta OpenType equivalente: 'ss15' |
| StylisticSet16 | `1936929078` | Conjunto estilístico 16 Etiqueta OpenType equivalente: 'ss16' |
| StylisticSet17 | `1936929079` | Conjunto estilístico 17 Etiqueta OpenType equivalente: 'ss17' |
| StylisticSet18 | `1936929080` | Conjunto estilístico 18 Etiqueta OpenType equivalente: 'ss18' |
| StylisticSet19 | `1936929081` | Conjunto estilístico 19 Etiqueta OpenType equivalente: 'ss19' |
| StylisticSet20 | `1936929328` | Conjunto estilístico 20 Etiqueta OpenType equivalente: 'ss20' |
| Kerning | `1801810542` | Ajusta la cantidad de espacio entre glifos, generalmente para proporcionar un espaciado ópticamente consistente entre ellos. Aunque una tipografía bien diseñada tiene un espaciado uniforme entre glifos en general, algunas combinaciones de glifos requieren un ajuste para mejorar la legibilidad. Además del ajuste estándar en la dirección horizontal, esta función puede proporcionar datos de kerning dependientes del tamaño a través de tablas de dispositivos, kerning "cross-stream" en la dirección del texto Y y ajuste de la ubicación del glifo independiente del ajuste avanzado. Tenga en cuenta que esta función puede aplicarse a series de más de dos glifos y no se utilizaría en fuentes monoespaciadas. Tenga en cuenta también que esta función no se aplica al texto establecido verticalmente. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#kern Etiqueta OpenType equivalente: 'kern' |

### Ver también

* espacio de nombres [Aspose.Words.Shaping](../../aspose.words.shaping/)
* asamblea [Aspose.Words](../../)
