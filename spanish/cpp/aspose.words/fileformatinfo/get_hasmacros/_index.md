---
title: "Aspose::Words::FileFormatInfo::get_HasMacros método"
linktitle: "get_HasMacros"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::FileFormatInfo::get_HasMacros método. Devuelve true si este documento contiene macros VBA en C++."
type: docs
weight: 3500
url: /es/cpp/aspose.words/fileformatinfo/get_hasmacros/
---
## FileFormatInfo::get_HasMacros method


Devuelve **true** si este documento contiene macros VBA.

```cpp
bool Aspose::Words::FileFormatInfo::get_HasMacros() const
```


## Ejemplos



Muestra cómo comprobar la presencia de macros VBA sin cargar el documento.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> fileFormatInfo = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Macro.docm");
ASSERT_TRUE(fileFormatInfo->get_HasMacros());
```

## Ver también

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
