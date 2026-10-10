---
title: "Aspose::Words::Saving::IFontSavingCallback interfaz"
linktitle: "IFontSavingCallback"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::IFontSavingCallback interfaz. Implemente esta interfaz si desea recibir notificaciones y controlar cómo Aspose.Words guarda fuentes al exportar un documento al formato HTML en C++."
type: docs
weight: 42000
url: /es/cpp/aspose.words.saving/ifontsavingcallback/
---
## IFontSavingCallback interface


Implemente esta interfaz si desea recibir notificaciones y controlar cómo Aspose.Words guarda fuentes al exportar un documento al formato HTML.

```cpp
class IFontSavingCallback : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| virtual [FontSaving](./fontsaving/)(System::SharedPtr\<Aspose::Words::Saving::FontSavingArgs\>) | Se llama cuando Aspose.Words está a punto de guardar un recurso de fuente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
