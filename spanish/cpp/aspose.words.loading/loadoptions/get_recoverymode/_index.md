---
title: "Aspose::Words::Loading::LoadOptions::get_RecoveryMode método"
linktitle: "get_RecoveryMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Loading::LoadOptions::get_RecoveryMode. Define cómo debe manejarse el documento si se producen errores durante la carga. Use esta propiedad para especificar si el sistema debe intentar recuperar el documento o seguir otro comportamiento definido. El valor predeterminado es TryRecover en C++."
type: docs
weight: 14500
url: /es/cpp/aspose.words.loading/loadoptions/get_recoverymode/
---
## LoadOptions::get_RecoveryMode method


Define cómo debe manejarse el documento si se producen errores durante la carga. Use esta propiedad para especificar si el sistema debe intentar recuperar el documento o seguir otro comportamiento definido. El valor predeterminado es [TryRecover](../../documentrecoverymode/).

```cpp
Aspose::Words::Loading::DocumentRecoveryMode Aspose::Words::Loading::LoadOptions::get_RecoveryMode() const
```


## Ejemplos



Muestra cómo intentar recuperar un documento si se produjeron errores durante la carga.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_RecoveryMode(Aspose::Words::Loading::DocumentRecoveryMode::TryRecover);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted footnotes.docx", loadOptions);
```

## Ver también

* Enum [DocumentRecoveryMode](../../documentrecoverymode/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
