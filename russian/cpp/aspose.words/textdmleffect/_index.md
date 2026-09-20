---
title: "перечисление Aspose::Words::TextDmlEffect"
linktitle: "TextDmlEffect"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::TextDmlEffect enum. Dml-эффект текста для текстовых прогонов в C++."
type: docs
weight: 122000
url: /ru/cpp/aspose.words/textdmleffect/
---
## TextDmlEffect enum


Эффект Dml текста для текстовых фрагментов.

```cpp
enum class TextDmlEffect
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Glow | 0 | Эффект свечения, при котором размытая цветная обводка добавляется за пределами краёв объекта. |
| Fill | 1 | Эффект наложения заливки. |
| Shadow | 2 | Эффект тени. |
| Outline | 3 | Эффект контура. |
| Effect3D | 4 | 3D-эффект. |
| Reflection | 5 | Эффект отражения. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
