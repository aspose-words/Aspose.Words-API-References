---
title: "método Aspose::Words::ImportFormatOptions::get_ForceCopyStyles"
linktitle: "get_ForceCopyStyles"
second_title: "Referencia de API de Aspose.Words para C++"
description: "método Aspose::Words::ImportFormatOptions::get_ForceCopyStyles. Obtiene o establece un valor booleano que indica si se deben copiar estilos en conflicto en modo KeepSourceFormatting. El valor predeterminado es false en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/importformatoptions/get_forcecopystyles/
---
## ImportFormatOptions::get_ForceCopyStyles method


Obtiene o establece un valor booleano que indica si se deben copiar estilos en conflicto en modo [KeepSourceFormatting](../../importformatmode/). El valor predeterminado es **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_ForceCopyStyles() const
```

## Observaciones


Por defecto, si ya existe un estilo coincidente en un documento de destino, el formato del estilo de origen se expande en atributos directos del nodo y el estilo de este nodo se restablece al valor predeterminado.

Cuando esta opción se establece en **true**, el estilo de origen se copiará forzadamente al documento de destino con un nombre único y se aplicará al nodo importado.

Nota, en este caso no se garantiza que el formato del nodo importado en el documento de destino se preserve.

## Ejemplos



Muestra cómo copiar forzadamente los estilos de origen con nombres únicos.
```cpp
// Ambos documentos contienen MyStyle1 y MyStyle2, MyStyle3 existe solo en un documento de origen.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Styles source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Styles destination.docx");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ForceCopyStyles(true);
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

System::SharedPtr<Aspose::Words::ParagraphCollection> paras = dstDoc->get_Sections()->idx_get(1)->get_Body()->get_Paragraphs();

ASSERT_EQ(paras->idx_get(0)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle1_0");
ASSERT_EQ(paras->idx_get(1)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle2_0");
ASSERT_EQ(paras->idx_get(2)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle3");
```

## Ver también

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
