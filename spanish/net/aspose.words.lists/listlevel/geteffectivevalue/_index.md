---
title: ListLevel.GetEffectiveValue
linktitle: GetEffectiveValue
articleTitle: GetEffectiveValue
second_title: Aspose.Words para .NET
description: Descubra el método GetEffectiveValue de ListLevel para recuperar fácilmente las representaciones de cadena de los elementos de la lista. ¡Personalícelo con opciones de formato y estilo numérico!
type: docs
weight: 190
url: /es/net/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel.GetEffectiveValue method

Informa la representación de cadena de la[`ListLevel`](../)objeto para el índice especificado del elemento de lista. Los parámetros especifican el[`NumberStyle`](../../../aspose.words/numberstyle/) y una cadena de formato opcional utilizada cuandoCustom se especifica.

```csharp
public static string GetEffectiveValue(int index, NumberStyle numberStyle, 
    string customNumberStyleFormat)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| index | Int32 | El índice del elemento de la lista (debe estar en el rango de 1 a 32767). |
| numberStyle | NumberStyle | El[`NumberStyle`](../../../aspose.words/numberstyle/) del[`ListLevel`](../) objeto. |
| customNumberStyleFormat | String | La cadena de formato opcional utilizada cuandoCustom se especifica (por ejemplo, "a, ç, ĝ, ..."). En otros casos, este parámetro debe ser`nulo` o vacío. |

### Valor_devuelto

La representación de cadena de la[`ListLevel`](../) objeto, descrito por el*numberStyle* parámetro y el*customNumberStyleFormat* parámetro, en el elemento de lista en la posición determinada por el*index* parámetro.

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentException | *customNumberStyleFormat* es`nulo` o vacío cuando el*numberStyle* es personalizado.-o- *customNumberStyleFormat* no es`nulo` o vacío cuando el*numberStyle* no es personalizado.-o- *customNumberStyleFormat* no es válido. |
| ArgumentOutOfRangeException | El índice está fuera de rango. |

## Ejemplos

Muestra cómo obtener el formato de una lista con el estilo de número personalizado.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// Podemos obtener el valor para el índice especificado del elemento de la lista.
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### Ver también

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [ListLevel](../)
* espacio de nombres [Aspose.Words.Lists](../../../aspose.words.lists/)
* asamblea [Aspose.Words](../../../)
