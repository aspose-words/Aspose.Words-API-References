---
title: "Aspose::Words::Drawing::OleFormat::get_SuggestedFileName método"
linktitle: "get_SuggestedFileName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::OleFormat::get_SuggestedFileName método. Obtiene el nombre de archivo sugerido para el objeto incrustado actual si deseas guardarlo en un archivo en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words.drawing/oleformat/get_suggestedfilename/
---
## OleFormat::get_SuggestedFileName method


Obtiene el nombre de archivo sugerido para el objeto incrustado actual si desea guardarlo en un archivo.

```cpp
System::String Aspose::Words::Drawing::OleFormat::get_SuggestedFileName()
```


## Ejemplos



Muestra cómo obtener el nombre de archivo sugerido de un objeto OLE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE shape.rtf");

auto oleShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->get_FirstSection()->get_Body()->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// Los objetos OLE pueden proporcionar un nombre de archivo y extensión sugeridos,
// que podemos usar al guardar el contenido del objeto en un archivo en el sistema de archivos local.
System::String suggestedFileName = oleShape->get_OleFormat()->get_SuggestedFileName();

ASSERT_EQ(u"CSV.csv", suggestedFileName);

{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + suggestedFileName, System::IO::FileMode::Create);
    oleShape->get_OleFormat()->Save(fileStream);
}
```

## Ver también

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
