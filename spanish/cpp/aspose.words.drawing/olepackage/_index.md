---
title: "Clase Aspose::Words::Drawing::OlePackage"
linktitle: "OlePackage"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Drawing::OlePackage. Permite acceder a las propiedades del paquete OLE. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.drawing/olepackage/
---
## OlePackage class


Permite acceder a las propiedades del paquete OLE. Para obtener más información, visite el artículo de documentación [Working with Ole Objects](https://docs.aspose.com/words/cpp/working-with-ole-objects/).

```cpp
class OlePackage : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_DisplayName](./get_displayname/)() const | Obtiene o establece el nombre para mostrar del paquete OLE. |
| [get_FileName](./get_filename/)() const | Obtiene o establece el nombre de archivo del paquete OLE. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DisplayName](./set_displayname/)(System::String) | Setter para [Aspose::Words::Drawing::OlePackage::get_DisplayName](./get_displayname/). |
| [set_FileName](./set_filename/)(System::String) | Setter para [Aspose::Words::Drawing::OlePackage::get_FileName](./get_filename/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
