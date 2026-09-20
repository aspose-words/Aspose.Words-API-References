---
title: "Aspose::Words::Drawing::OleFormat::get_AutoUpdate método"
linktitle: "get_AutoUpdate"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::OleFormat::get_AutoUpdate método. Especifica si el vínculo al objeto OLE se actualiza automáticamente o no en Microsoft Word en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.drawing/oleformat/get_autoupdate/
---
## OleFormat::get_AutoUpdate method


Especifica si el vínculo al objeto OLE se actualiza automáticamente o no en Microsoft Word.

```cpp
bool Aspose::Words::Drawing::OleFormat::get_AutoUpdate()
```

## Observaciones


El valor predeterminado es **false**.

## Ejemplos



Muestra cómo extraer objetos OLE incrustados en archivos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE spreadsheet.docm");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// El objeto OLE en la primera forma es una hoja de cálculo de Microsoft Excel.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shape->get_OleFormat();

ASSERT_EQ(u"Excel.Sheet.12", oleFormat->get_ProgId());

// Nuestro objeto no se actualiza automáticamente ni está bloqueado contra actualizaciones.
ASSERT_FALSE(oleFormat->get_AutoUpdate());
ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLocked());

// Si planeamos guardar el objeto OLE en un archivo en el sistema de archivos local,
// podemos usar la propiedad "SuggestedExtension" para determinar qué extensión de archivo aplicar al archivo.
ASSERT_EQ(u".xlsx", oleFormat->get_SuggestedExtension());

// A continuación se presentan dos formas de guardar un objeto OLE en un archivo en el sistema de archivos local.
// 1 -  Guárdalo mediante un flujo:
{
    auto fs = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"OLE spreadsheet extracted via stream" + oleFormat->get_SuggestedExtension(), System::IO::FileMode::Create);
    oleFormat->Save(fs);
}

// 2 -  Guárdalo directamente en un nombre de archivo:
oleFormat->Save(get_ArtifactsDir() + u"OLE spreadsheet saved directly" + oleFormat->get_SuggestedExtension());
```

## Ver también

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
