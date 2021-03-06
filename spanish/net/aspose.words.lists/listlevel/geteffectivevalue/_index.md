---
title: GetEffectiveValue
second_title: Referencia de API de Aspose.Words para .NET
description: Reporta la representación de cadena delListLevelaspose.words.lists/listlevel objeto para el índice especificado del elemento de la lista. Los parámetros especifican elNumberStyleaspose.words/numberstyle y un formato opcional string utilizado cuandoCustom se especifica.
type: docs
weight: 190
url: /es/net/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel.GetEffectiveValue method

Reporta la representación de cadena del[`ListLevel`](../../listlevel) objeto para el índice especificado del elemento de la lista. Los parámetros especifican el[`NumberStyle`](../../../aspose.words/numberstyle) y un formato opcional string utilizado cuandoCustom se especifica.

```csharp
public static string GetEffectiveValue(int index, NumberStyle numberStyle, 
    string customNumberStyleFormat)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| index | Int32 | El índice del elemento de la lista (debe estar en el rango de 1 a 32767). |
| numberStyle | NumberStyle | El[`NumberStyle`](../../../aspose.words/numberstyle) del[`ListLevel`](../../listlevel) objeto. |
| customNumberStyleFormat | String | La cadena de formato opcional utilizada cuandoCustom se especifica (por ejemplo, "a, ç, ĝ, ..."). En otros casos, este parámetro debe ser nulo o vacío. |

### Valor_devuelto

La representación de cadena del[`ListLevel`](../../listlevel) objeto, descrito por el parámetro numberStyle y el parámetro customNumberStyleFormat, en el elemento de la lista en la posición determinada por el parámetro index.

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentException | customNumberStyleFormat es nulo o está vacío cuando numberStyle es personalizado.-o- customNumberStyleFormat no es nulo o está vacío cuando numberStyle no es personalizado.-o- customNumberStyleFormat no es válido. |
| ArgumentOutOfRangeException | el índice está fuera de rango. |

### Ejemplos

Muestra cómo obtener el formato de una lista con el estilo de número personalizado.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// Podemos obtener valor para el índice especificado del elemento de la lista.
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### Ver también

* enum [NumberStyle](../../../aspose.words/numberstyle)
* class [ListLevel](../../listlevel)
* espacio de nombres [Aspose.Words.Lists](../../listlevel)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
