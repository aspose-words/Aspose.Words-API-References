---
title: "Aspose::Words::Drawing::OlePackage::get_FileName método"
linktitle: "get_FileName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::OlePackage::get_FileName método. Obtiene o establece el nombre de archivo del paquete OLE en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.drawing/olepackage/get_filename/
---
## OlePackage::get_FileName method


Obtiene o establece el nombre de archivo del paquete OLE.

```cpp
System::String Aspose::Words::Drawing::OlePackage::get_FileName() const
```


## Ejemplos



Muestra cómo insertar un objeto OLE en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Los objetos OLE nos permiten abrir otros archivos en el sistema de archivos local usando otra aplicación instalada
// en nuestro sistema operativo al hacer doble clic en la forma que contiene el objeto OLE en el cuerpo del documento.
// En este caso, nuestro archivo externo será un archivo ZIP.
System::ArrayPtr<uint8_t> zipFileBytes = System::IO::File::ReadAllBytes(get_DatabaseDir() + u"cat001.zip");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(zipFileBytes);
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObject(stream, u"Package", true, nullptr);

    shape->get_OleFormat()->get_OlePackage()->set_FileName(u"Package file name.zip");
    shape->get_OleFormat()->get_OlePackage()->set_DisplayName(u"Package display name.zip");
}

doc->Save(get_ArtifactsDir() + u"Shape.InsertOlePackage.docx");
```

## Ver también

* Class [OlePackage](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
