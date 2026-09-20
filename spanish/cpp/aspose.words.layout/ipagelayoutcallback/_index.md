---
title: "Aspose::Words::Layout::IPageLayoutCallback interface"
linktitle: "IPageLayoutCallback"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Layout::IPageLayoutCallback interface. Implemente esta interfaz si desea tener su propio método personalizado llamado durante la construcción y renderizado del modelo de diseño de página en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface


Implemente esta interfaz si desea tener su propio método personalizado llamado durante la construcción y renderizado del modelo de diseño de página.

```cpp
class IPageLayoutCallback : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Layout::PageLayoutCallbackArgs\>) | Esto se llama para notificar el progreso de la construcción y renderizado del diseño. |
| static [Type](./type/)() |  |
## Observaciones


El uso principal de esta interfaz es permitir que el código de la aplicación aborta el proceso de construcción.

Es posible construir el modelo de diseño de página solo para unas pocas páginas al inicio del documento, luego abortar el proceso y renderizar solo lo que ya se ha construido.

Sin embargo, tenga en cuenta que los resultados del renderizado pueden no coincidir con lo que se habría renderizado para cada página si el proceso hubiera finalizado.

Esta técnica puede no funcionar para todos los documentos o puede fallar completamente.

## Ver también

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
