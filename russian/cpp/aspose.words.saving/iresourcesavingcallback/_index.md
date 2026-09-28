---
title: "Aspose::Words::Saving::IResourceSavingCallback interface"
linktitle: "IResourceSavingCallback"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::IResourceSavingCallback interface. Реализуйте этот интерфейс, если хотите контролировать, как Aspose.Words сохраняет внешние ресурсы (изображения, шрифты и css) при сохранении документа в фиксированный HTML‑страницы или SVG на C++."
type: docs
weight: 45000
url: /ru/cpp/aspose.words.saving/iresourcesavingcallback/
---
## IResourceSavingCallback interface


Реализуйте этот интерфейс, если вы хотите контролировать, как Aspose.Words сохраняет внешние ресурсы (изображения, шрифты и css) при сохранении документа в фиксированный HTML или SVG.

```cpp
class IResourceSavingCallback : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [ResourceSaving](./resourcesaving/)(System::SharedPtr\<Aspose::Words::Saving::ResourceSavingArgs\>) | Вызывается, когда Aspose.Words сохраняет внешний ресурс в форматы фиксированного HTML или SVG. |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
