---
title: "Aspose::Words::Loading::DocumentRecoveryMode enum"
linktitle: "DocumentRecoveryMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Loading::DocumentRecoveryMode enum. Especifica las opciones de recuperación disponibles cuando un documento encuentra errores durante la carga en C++."
type: docs
weight: 13500
url: /es/cpp/aspose.words.loading/documentrecoverymode/
---
## DocumentRecoveryMode enum


Especifica las opciones de recuperación disponibles cuando un documento encuentra errores durante la carga.

```cpp
enum class DocumentRecoveryMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | No se intenta ninguna recuperación. Si el documento es inválido, la carga fallará con un error. |
| TryRecover | 1 | Intenta recuperar el documento mientras preserva la mayor cantidad de datos posible. |


## Ejemplos



Muestra cómo intentar recuperar un documento si se produjeron errores durante la carga.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_RecoveryMode(Aspose::Words::Loading::DocumentRecoveryMode::TryRecover);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted footnotes.docx", loadOptions);
```

## Ver también

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
