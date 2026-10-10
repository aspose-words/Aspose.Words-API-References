---
title: "Aspose::Words::StyleCollection::AddCopy método"
linktitle: "AddCopy"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::StyleCollection::AddCopy método. Copia un estilo en esta colección en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/stylecollection/addcopy/
---
## StyleCollection::AddCopy method


Copia un estilo en esta colección.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::AddCopy(const System::SharedPtr<Aspose::Words::Style> &style)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| style | const System::SharedPtr\<Aspose::Words::Style\>\& | [Style](../../style/) a copiar. |

### ReturnValue

Estilo copiado listo para su uso.
## Observaciones


[Style](../../style/) to be copied can belong to the same document as well as to different document.

El estilo vinculado se ha copiado.

Este método no copia los estilos base.

Si la colección ya contiene un estilo con el mismo nombre, entonces se genera automáticamente un nuevo nombre añadiendo el sufijo "_number" a partir de 0, p. ej. "Normal_0", "Heading 1_1", etc. Use el setter [Name](../../style/get_name/) para cambiar el nombre del estilo importado.

## Ejemplos



Muestra cómo clonar el estilo de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// El método AddCopy crea una copia del estilo especificado y
// genera automáticamente un nuevo nombre para el estilo, como "Heading 1_0".
System::SharedPtr<Aspose::Words::Style> newStyle = doc->get_Styles()->AddCopy(doc->get_Styles()->idx_get(u"Heading 1"));

// Utilice la propiedad "Name" del estilo para cambiar el nombre identificador del estilo.
newStyle->set_Name(u"My Heading 1");

// Nuestro documento ahora tiene dos estilos de apariencia idéntica con nombres diferentes.
// Cambiar la configuración de uno de los estilos no afecta al otro.
newStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

ASSERT_EQ(u"My Heading 1", newStyle->get_Name());
ASSERT_EQ(u"Heading 1", doc->get_Styles()->idx_get(u"Heading 1")->get_Name());

ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Type(), newStyle->get_Type());
ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Name(), newStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Size(), newStyle->get_Font()->get_Size());
ASPOSE_ASSERT_NE(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Color(), newStyle->get_Font()->get_Color());
```


Muestra cómo importar un estilo de un documento a otro documento diferente.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();

// Cree un estilo personalizado para el documento de origen.
System::SharedPtr<Aspose::Words::Style> srcStyle = srcDoc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
srcStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

// Importe el estilo personalizado del documento de origen al documento de destino.
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> newStyle = dstDoc->get_Styles()->AddCopy(srcStyle);

// El estilo importado tiene una apariencia idéntica a su estilo de origen.
ASSERT_EQ(u"MyStyle", newStyle->get_Name());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), newStyle->get_Font()->get_Color().ToArgb());
```

## Ver también

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
