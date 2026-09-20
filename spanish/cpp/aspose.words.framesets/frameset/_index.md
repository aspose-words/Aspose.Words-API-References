---
title: "Aspose::Words::Framesets::Frameset class"
linktitle: "Frameset"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Framesets::Frameset class. Representa una página de marcos o un solo marco en una página de marcos. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.framesets/frameset/
---
## Frameset class


Representa una página de marcos o un solo marco en una página de marcos. Para obtener más información, visite el artículo de documentación [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class Frameset : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Frameset](./frameset/)() |  |
| [get_ChildFramesets](./get_childframesets/)() const | Obtiene la colección de marcos secundarios y páginas de marcos. |
| [get_FrameDefaultUrl](./get_framedefaulturl/)() | Obtiene o establece la URL de la página web o el nombre de archivo del documento que se mostrará en este marco. |
| [get_IsFrameLinkToFile](./get_isframelinktofile/)() | Obtiene o establece un valor que indica si la página web o el nombre de archivo del documento especificado en la propiedad [FrameDefaultUrl](./get_framedefaulturl/) es un recurso externo con el que el marco está vinculado. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FrameDefaultUrl](./set_framedefaulturl/)(const System::String\&) | Setter para [Aspose::Words::Framesets::Frameset::get_FrameDefaultUrl](./get_framedefaulturl/). |
| [set_IsFrameLinkToFile](./set_isframelinktofile/)(bool) | Setter para [Aspose::Words::Framesets::Frameset::get_IsFrameLinkToFile](./get_isframelinktofile/). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo acceder a los frames en la página.
```cpp
// El documento contiene varios frames con enlaces a otros documentos.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Frameset.docx");

ASSERT_EQ(3, doc->get_Frameset()->get_ChildFramesets()->get_Count());
// Podemos comprobar la URL predeterminada (una URL de página web o documento local) o si el frame es un recurso externo.
ASSERT_EQ(u"https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx", doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->get_FrameDefaultUrl());
ASSERT_TRUE(doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->get_IsFrameLinkToFile());

ASSERT_EQ(u"Document.docx", doc->get_Frameset()->get_ChildFramesets()->idx_get(1)->get_FrameDefaultUrl());
ASSERT_FALSE(doc->get_Frameset()->get_ChildFramesets()->idx_get(1)->get_IsFrameLinkToFile());

// Cambiar propiedades de uno de nuestros frames.
doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->set_FrameDefaultUrl(u"https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx");
doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->set_IsFrameLinkToFile(false);
```

## Ver también

* Namespace [Aspose::Words::Framesets](../)
* Library [Aspose.Words for C++](../../)
