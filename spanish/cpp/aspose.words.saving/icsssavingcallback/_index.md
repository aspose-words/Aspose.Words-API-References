---
title: "Interfaz Aspose::Words::Saving::ICssSavingCallback"
linktitle: "ICssSavingCallback"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Interfaz Aspose::Words::Saving::ICssSavingCallback. Implemente esta interfaz si desea controlar cómo Aspose.Words guarda CSS (Cascading Style Sheet) al guardar un documento en HTML en C++."
type: docs
weight: 39000
url: /es/cpp/aspose.words.saving/icsssavingcallback/
---
## ICssSavingCallback interface


Implemente esta interfaz si desea controlar cómo Aspose.Words guarda CSS (Cascading [Style](../../aspose.words/style/) Sheet) al guardar un documento en HTML.

```cpp
class ICssSavingCallback : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| virtual [CssSaving](./csssaving/)(System::SharedPtr\<Aspose::Words::Saving::CssSavingArgs\>) | Se llama cuando Aspose.Words guarda una hoja CSS (Cascading [Style](../../aspose.words/style/) Sheet). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
