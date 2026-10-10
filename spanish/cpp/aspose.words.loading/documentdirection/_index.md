---
title: "Enumeración Aspose::Words::Loading::DocumentDirection"
linktitle: "DocumentDirection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Enumeración Aspose::Words::Loading::DocumentDirection. Permite especificar la dirección del flujo de texto en un documento en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words.loading/documentdirection/
---
## DocumentDirection enum


Permite especificar la dirección del flujo de texto en un documento.

```cpp
enum class DocumentDirection
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| LeftToRight | 0 | Dirección de izquierda a derecha. |
| RightToLeft | 1 | Dirección de derecha a izquierda. |
| Auto | 2 | Dirección de detección automática. |


## Ejemplos



Muestra cómo detectar la dirección del texto en un documento de texto plano.
```cpp
// Cree un objeto "TxtLoadOptions", que podemos pasar al constructor de un documento
// para modificar cómo cargamos un documento de texto plano.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Establezca la propiedad "DocumentDirection" a "DocumentDirection.Auto" para detectar automáticamente
// la dirección de cada párrafo de texto que Aspose.Words carga desde texto plano.
// La propiedad "Bidi" de cada párrafo almacenará su dirección.
loadOptions->set_DocumentDirection(Aspose::Words::Loading::DocumentDirection::Auto);

// Detectar texto hebreo como de derecha a izquierda.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Hebrew text.txt", loadOptions);

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());

// Detectar texto inglés como de derecha a izquierda.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());
```

## Ver también

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
