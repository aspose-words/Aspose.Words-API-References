---
title: "Aspose::Words::Font::get_NumberSpacing метод"
linktitle: "get_NumberSpacing"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_NumberSpacing. Получает или задает тип интервала цифры, отображаемой в C++."
type: docs
weight: 30500
url: /ru/cpp/aspose.words/font/get_numberspacing/
---
## Font::get_NumberSpacing method


Получает или задает тип интервала цифры, отображаемой.

```cpp
Aspose::Words::NumSpacing Aspose::Words::Font::get_NumberSpacing()
```


## Примеры



Показывает, как задать тип интервала цифры.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Этот эффект поддерживается только в более новых версиях MS Word.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2019);

builder->Write(u"1 ");
builder->Write(u"This is an example");

System::SharedPtr<Aspose::Words::Run> run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
if (run->get_Font()->get_NumberSpacing() == Aspose::Words::NumSpacing::Default)
{
    run->get_Font()->set_NumberSpacing(Aspose::Words::NumSpacing::Proportional);
}

doc->Save(get_ArtifactsDir() + u"Fonts.NumberSpacing.docx");
```

## См. также

* Enum [NumSpacing](../../numspacing/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
