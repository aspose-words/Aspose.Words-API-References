---
title: "Aspose::Words::Saving::PageSavingArgs-klass"
linktitle: "PageSavingArgs"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PageSavingArgs-klass. Tillhandahåller data för PageSaving()-händelsen. För att läsa mer, besök dokumentationsartikeln i C++."
type: docs
weight: 19000
url: /sv/cpp/aspose.words.saving/pagesavingargs/
---
## PageSavingArgs class


Tillhandahåller data för [PageSaving()](../ipagesavingcallback/pagesaving/)‑händelsen. För att läsa mer, besök [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) dokumentationsartikel.

```cpp
class PageSavingArgs : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_KeepPageStreamOpen](./get_keeppagestreamopen/)() const | Anger om Aspose.Words ska hålla strömmen öppen eller stänga den efter att ha sparat en dokumentsida. |
| [get_PageFileName](./get_pagefilename/)() const | Hämtar filnamnet där dokumentsidan kommer att sparas. |
| [get_PageIndex](./get_pageindex/)() const | Aktuellt sidindex. |
| [get_PageStream](./get_pagestream/)() const | Tillåter att ange strömmen där dokumentsidan kommer att sparas. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageSavingArgs](./pagesavingargs/)() |  |
| [set_KeepPageStreamOpen](./set_keeppagestreamopen/)(bool) | Inställare för [Aspose::Words::Saving::PageSavingArgs::get_KeepPageStreamOpen](./get_keeppagestreamopen/). |
| [set_PageFileName](./set_pagefilename/)(const System::String\&) | Ställer in filnamnet där dokumentsidan kommer att sparas. |
| [set_PageStream](./set_pagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Inställare för [Aspose::Words::Saving::PageSavingArgs::get_PageStream](./get_pagestream/). |
| [set_PageStream](./set_pagestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
