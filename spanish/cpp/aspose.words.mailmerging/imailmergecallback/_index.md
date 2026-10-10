---
title: "Aspose::Words::MailMerging::IMailMergeCallback interface"
linktitle: "IMailMergeCallback"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::MailMerging::IMailMergeCallback interface. Implemente esta interfaz si desea recibir notificaciones mientras se realiza la combinación de correspondencia en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.mailmerging/imailmergecallback/
---
## IMailMergeCallback interface


Implemente esta interfaz si desea recibir notificaciones mientras se realiza la combinación de correspondencia.

```cpp
class IMailMergeCallback : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [TagsReplaced](./tagsreplaced/)() | Se llama cuando las etiquetas de texto \"mustache\" se reemplazan con campos MERGEFIELD. |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
