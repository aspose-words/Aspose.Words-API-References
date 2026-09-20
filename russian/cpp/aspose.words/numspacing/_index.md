---
title: "Aspose::Words::NumSpacing enum"
linktitle: "NumSpacing"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::NumSpacing. Задает возможные значения, в которых может отображаться интервал между цифрами в C++."
type: docs
weight: 103500
url: /ru/cpp/aspose.words/numspacing/
---
## NumSpacing enum


Указывает возможные значения, в которых может отображаться интервал между цифрами.

```cpp
enum class NumSpacing
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Default | 0 | Указывает, что цифры отображаются в форме по умолчанию шрифта. |
| Proportional | 1 | Указывает, что формы цифр, разработанные как пропорционально распределённые, отображаются, если шрифт поддерживает их. |
| Tabular | 2 | Указывает, что формы цифр, оформленные как табличные, отображаются, если шрифт поддерживает их. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
