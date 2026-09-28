---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance метод"
linktitle: "get_Appearance"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance метод. Получает или задает внешний вид структурированного тега документа в C++."
type: docs
weight: 1500
url: /ru/cpp/aspose.words.markup/istructureddocumenttag/get_appearance/
---
## IStructuredDocumentTag::get_Appearance method


Получает или задает внешний вид структурированного тега документа.

```cpp
virtual Aspose::Words::Markup::SdtAppearance Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance()=0
```


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

* Enum [SdtAppearance](../../sdtappearance/)
* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
