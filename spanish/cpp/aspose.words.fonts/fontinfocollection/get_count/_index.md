---
title: "Aspose::Words::Fonts::FontInfoCollection::get_Count método"
linktitle: "get_Count"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FontInfoCollection::get_Count método. Obtiene el número de elementos contenidos en la colección en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.fonts/fontinfocollection/get_count/
---
## FontInfoCollection::get_Count method


Obtiene el número de elementos contenidos en la colección.

```cpp
int32_t Aspose::Words::Fonts::FontInfoCollection::get_Count()
```


## Ejemplos



Muestra información sobre las fuentes que están presentes en el documento en blanco.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un documento en blanco contiene 3 fuentes predeterminadas. Cada fuente en el documento
// tendrá un objeto FontInfo correspondiente que contiene detalles sobre esa fuente.
ASSERT_EQ(3, doc->get_FontInfos()->get_Count());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Times New Roman"));
ASSERT_EQ(204, doc->get_FontInfos()->idx_get(u"Times New Roman")->get_Charset());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Symbol"));
ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Arial"));
```

## Ver también

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
