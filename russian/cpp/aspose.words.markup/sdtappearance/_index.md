---
title: "Aspose::Words::Markup::SdtAppearance enum"
linktitle: "SdtAppearance"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::SdtAppearance enum. Указывает внешний вид структурного тега документа в C++."
type: docs
weight: 18000
url: /ru/cpp/aspose.words.markup/sdtappearance/
---
## SdtAppearance enum


Указывает внешний вид структурного тега документа.

```cpp
enum class SdtAppearance
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| BoundingBox | 0 | Представляет структурный тег документа, отображаемый в виде затенённого прямоугольника или ограничивающего блока. |
| Tags | 1 | Представляет структурный тег документа, отображаемый в виде начального и конечного маркеров. |
| Скрытый | 2 | Представляет структурный тег документа, который не отображается. |
| Default | n/a | По умолчанию — [BoundingBox](./). |


## Примеры



Показывает, как отобразить тег вокруг содержимого.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

if (tag->get_Appearance() == Aspose::Words::Markup::SdtAppearance::Hidden)
{
    tag->set_Appearance(Aspose::Words::Markup::SdtAppearance::Tags);
}
```

## См. также

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
