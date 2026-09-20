---
title: "Aspose::Words::Framesets::FramesetCollection::idx_get método"
linktitle: "idx_get"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Framesets::FramesetCollection::idx_get método. Obtiene un marco o página de marcos en el índice especificado en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.framesets/framesetcollection/idx_get/
---
## FramesetCollection::idx_get method


Obtiene un frame o página de frames en el índice especificado.

```cpp
System::SharedPtr<Aspose::Words::Framesets::Frameset> Aspose::Words::Framesets::FramesetCollection::idx_get(int32_t index)
```


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

* Class [Frameset](../../frameset/)
* Class [FramesetCollection](../)
* Namespace [Aspose::Words::Framesets](../../)
* Library [Aspose.Words for C++](../../../)
