---
title: "Aspose::Words::Saving::DownsampleOptions class"
linktitle: "DownsampleOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::DownsampleOptions class. Позволяет задавать параметры понижения дискретизации. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.saving/downsampleoptions/
---
## DownsampleOptions class


Позволяет указать параметры понижения дискретизации. Чтобы узнать больше, посетите статью документации [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class DownsampleOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [DownsampleOptions](./downsampleoptions/)() |  |
| [get_DownsampleImages](./get_downsampleimages/)() const | Указывает, следует ли понижать дискретизацию изображений. |
| [get_Resolution](./get_resolution/)() const | Указывает разрешение в пикселях на дюйм, до которого следует понижать дискретизацию изображений. |
| [get_ResolutionThreshold](./get_resolutionthreshold/)() const | Указывает пороговое разрешение в пикселях на дюйм. Если разрешение изображения в документе меньше порогового значения, алгоритм понижения дискретизации не будет применён. Значение 0 означает, что проверка порога не используется, и все изображения, которые можно уменьшить в размере, понижаются. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DownsampleImages](./set_downsampleimages/)(bool) | Указывает, следует ли понижать дискретизацию изображений. |
| [set_Resolution](./set_resolution/)(int32_t) | Указывает разрешение в пикселях на дюйм, до которого следует понижать дискретизацию изображений. |
| [set_ResolutionThreshold](./set_resolutionthreshold/)(int32_t) | Сеттер для [Aspose::Words::Saving::DownsampleOptions::get_ResolutionThreshold](./get_resolutionthreshold/). |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
