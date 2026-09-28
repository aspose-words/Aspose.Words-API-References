---
title: "Aspose::Words::Rendering::NodeRendererBase::GetOpaqueBoundsInPixels method"
linktitle: "GetOpaqueBoundsInPixels"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Rendering::NodeRendererBase::GetOpaqueBoundsInPixels method. Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/
---
## NodeRendererBase::GetOpaqueBoundsInPixels(float, float) method


Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения.

```cpp
System::Drawing::Rectangle Aspose::Words::Rendering::NodeRendererBase::GetOpaqueBoundsInPixels(float scale, float dpi)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| scale | float | Коэффициент масштабирования (1.0 соответствует 100%). |
| dpi | float | Разрешение для преобразования из пунктов в пиксели (точек на дюйм). |

### ReturnValue

Непрозрачный прямоугольник фигуры в пикселях.
## Примечания


Этот метод преобразует [OpaqueBoundsInPoints](../get_opaqueboundsinpoints/) в прямоугольник в пикселях и полезен, когда вы хотите создать bitmap для рендеринга фигуры только с её непрозрачной частью.

## Примеры



Показывает, как измерять и масштабировать фигуры.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));
auto renderer = System::MakeObject<Aspose::Words::Rendering::OfficeMathRenderer>(officeMath);

// Проверьте размер изображения, которое объект OfficeMath создаст при его отрисовке.
ASSERT_NEAR(122.0f, renderer->get_SizeInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_SizeInPoints().get_Height(), 0.15f);

ASSERT_NEAR(122.0f, renderer->get_BoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_BoundsInPoints().get_Height(), 0.15f);

// Фигуры с прозрачными частями могут содержать разные значения в свойствах "OpaqueBoundsInPoints".
ASSERT_NEAR(119.5f, renderer->get_OpaqueBoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(14.2f, renderer->get_OpaqueBoundsInPoints().get_Height(), 0.1f);

// Получите размер фигуры в пикселях с линейным масштабированием до указанного DPI.
System::Drawing::Rectangle bounds = renderer->GetBoundsInPixels(1.0f, 96.0f);
System::String dpi96 = u"DPI 96";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96);
ASSERT_EQ(18, bounds.get_Height()) << (dpi96);

// Получите размер фигуры в пикселях, но с разным DPI для горизонтального и вертикального измерений.
bounds = renderer->GetBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150 = u"DPI 96 150";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96150);
ASSERT_EQ(27, bounds.get_Height()) << (dpi96150);

// Непрозрачные границы также могут здесь различаться.
bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f);
System::String dpi96Opaque = u"DPI 96 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96Opaque);
ASSERT_EQ(19, bounds.get_Height()) << (dpi96Opaque);

bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150Opaque = u"DPI 96 150 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96150Opaque);
ASSERT_EQ(29, bounds.get_Height()) << (dpi96150Opaque);
```

## См. также

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::GetOpaqueBoundsInPixels(float, float, float) method


Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения.

```cpp
System::Drawing::Rectangle Aspose::Words::Rendering::NodeRendererBase::GetOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| scale | float | Коэффициент масштабирования (1.0 соответствует 100%). |
| horizontalDpi | float | Горизонтальное разрешение для преобразования из пунктов в пиксели (точек на дюйм). |
| verticalDpi | float | Вертикальное разрешение для преобразования из пунктов в пиксели (точек на дюйм). |

### ReturnValue

Непрозрачный прямоугольник фигуры в пикселях.
## Примечания


Этот метод преобразует [OpaqueBoundsInPoints](../get_opaqueboundsinpoints/) в прямоугольник в пикселях и полезен, когда вы хотите создать bitmap для рендеринга фигуры только с её непрозрачной частью.

## Примеры



Показывает, как измерять и масштабировать фигуры.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));
auto renderer = System::MakeObject<Aspose::Words::Rendering::OfficeMathRenderer>(officeMath);

// Проверьте размер изображения, которое объект OfficeMath создаст при его отрисовке.
ASSERT_NEAR(122.0f, renderer->get_SizeInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_SizeInPoints().get_Height(), 0.15f);

ASSERT_NEAR(122.0f, renderer->get_BoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_BoundsInPoints().get_Height(), 0.15f);

// Фигуры с прозрачными частями могут содержать разные значения в свойствах "OpaqueBoundsInPoints".
ASSERT_NEAR(119.5f, renderer->get_OpaqueBoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(14.2f, renderer->get_OpaqueBoundsInPoints().get_Height(), 0.1f);

// Получите размер фигуры в пикселях с линейным масштабированием до указанного DPI.
System::Drawing::Rectangle bounds = renderer->GetBoundsInPixels(1.0f, 96.0f);
System::String dpi96 = u"DPI 96";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96);
ASSERT_EQ(18, bounds.get_Height()) << (dpi96);

// Получите размер фигуры в пикселях, но с разным DPI для горизонтального и вертикального измерений.
bounds = renderer->GetBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150 = u"DPI 96 150";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96150);
ASSERT_EQ(27, bounds.get_Height()) << (dpi96150);

// Непрозрачные границы также могут здесь различаться.
bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f);
System::String dpi96Opaque = u"DPI 96 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96Opaque);
ASSERT_EQ(19, bounds.get_Height()) << (dpi96Opaque);

bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150Opaque = u"DPI 96 150 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96150Opaque);
ASSERT_EQ(29, bounds.get_Height()) << (dpi96150Opaque);
```

## См. также

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
