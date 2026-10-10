---
title: "Metodo Aspose::Words::FileFormatInfo::get_HasMacros"
linktitle: "get_HasMacros"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::FileFormatInfo::get_HasMacros. Restituisce true se questo documento contiene macro VBA in C++."
type: docs
weight: 3500
url: /it/cpp/aspose.words/fileformatinfo/get_hasmacros/
---
## FileFormatInfo::get_HasMacros method


Restituisce **true** se questo documento contiene macro VBA.

```cpp
bool Aspose::Words::FileFormatInfo::get_HasMacros() const
```


## Esempi



Mostra come verificare la presenza di macro VBA senza caricare il documento.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> fileFormatInfo = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Macro.docm");
ASSERT_TRUE(fileFormatInfo->get_HasMacros());
```

## Vedi anche

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
