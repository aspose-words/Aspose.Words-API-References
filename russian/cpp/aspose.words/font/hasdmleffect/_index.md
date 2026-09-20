---
title: "Метод Aspose::Words::Font::HasDmlEffect"
linktitle: "HasDmlEffect"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::HasDmlEffect. Проверяет, применён ли конкретный эффект текста DrawingML в C++."
type: docs
weight: 58000
url: /ru/cpp/aspose.words/font/hasdmleffect/
---
## Font::HasDmlEffect method


Проверяет, применён ли конкретный эффект текста DrawingML.

```cpp
bool Aspose::Words::Font::HasDmlEffect(Aspose::Words::TextDmlEffect dmlEffectType)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| dmlEffectType | Aspose::Words::TextDmlEffect | Тип эффекта текста DrawingML. |

### ReturnValue

**true** if particular DrawingML text effect is applied.

## Примеры



Показывает, как проверить, отображает ли прогон эффект текста DrawingML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DrawingML text effects.docx");

System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();

ASSERT_TRUE(runs->idx_get(0)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Shadow));
ASSERT_TRUE(runs->idx_get(1)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Shadow));
ASSERT_TRUE(runs->idx_get(2)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Reflection));
ASSERT_TRUE(runs->idx_get(3)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Effect3D));
ASSERT_TRUE(runs->idx_get(4)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Fill));
```

## См. также

* Enum [TextDmlEffect](../../textdmleffect/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
