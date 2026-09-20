---
title: "Aspose::Words::Document::JoinRunsWithSameFormatting method"
linktitle: "JoinRunsWithSameFormatting"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::JoinRunsWithSameFormatting method. Une los runs con el mismo formato en todos los párrafos del documento en C++."
type: docs
weight: 65000
url: /es/cpp/aspose.words/document/joinrunswithsameformatting/
---
## Document::JoinRunsWithSameFormatting method


Une secuencias con el mismo formato en todos los párrafos del documento.

```cpp
int32_t Aspose::Words::Document::JoinRunsWithSameFormatting()
```


### ReturnValue

Número de uniones realizadas. Cuando se unen **N** runs adyacentes, cuentan como **N - 1** uniones.
## Observaciones


Este es un método de optimización. Algunos documentos contienen runs adyacentes con el mismo formato. Normalmente ocurre si un documento fue editado intensamente de forma manual. Puede reducir el tamaño del documento y acelerar el procesamiento posterior al unir estos runs.

La operación verifica cada nodo [Paragraph](../../paragraph/) en el documento en busca de nodos [Run](../../run/) adyacentes que tengan propiedades idénticas. Ignora los identificadores únicos utilizados para rastrear las sesiones de edición de la creación y modificación de runs. El primer run en cada secuencia de unión acumula todo el texto. Los runs restantes se eliminan del documento.

## Ejemplos



Muestra cómo unir runs en un documento para reducir runs innecesarios.
```cpp
// Abra un documento que contenga runs de texto adyacentes con formato idéntico,
// lo cual ocurre comúnmente si editamos el mismo párrafo varias veces en Microsoft Word.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Si cualquier número de estos runs son adyacentes con formato idéntico,
// entonces el documento puede simplificarse.
ASSERT_EQ(317, doc->GetChildNodes(Aspose::Words::NodeType::Run, true)->get_Count());

// Combine dichos runs con este método y verifique el número de uniones de runs que se realizarán.
ASSERT_EQ(121, doc->JoinRunsWithSameFormatting());

// El número de uniones y el número de runs que tenemos después de la unión
// deberían sumar el número de runs que teníamos inicialmente.
ASSERT_EQ(196, doc->GetChildNodes(Aspose::Words::NodeType::Run, true)->get_Count());
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
