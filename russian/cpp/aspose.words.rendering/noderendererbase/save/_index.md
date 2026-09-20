---
title: "Aspose::Words::Rendering::NodeRendererBase::Save method"
linktitle: "Save"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Rendering::NodeRendererBase::Save method. Отрисовывает форму в изображение и сохраняет в поток в C++."
type: docs
weight: 13000
url: /ru/cpp/aspose.words.rendering/noderendererbase/save/
---
## NodeRendererBase::Save(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) method


Отрисовывает фигуру в изображение и сохраняет в поток.

```cpp
void Aspose::Words::Rendering::NodeRendererBase::Save(const System::SharedPtr<System::IO::Stream> &stream, System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> saveOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | Поток, в который сохраняется изображение формы. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\> | Указывает параметры, которые контролируют, как форма отрисовывается и сохраняется. Может быть **null**. Если это **null**, изображение будет сохранено в формате PNG. |

## Примеры



Показывает, как использовать рендерер формы для экспорта форм в файлы в локальной файловой системе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(7, shapes->get_Length());

// В документе 7 форм, включая одну групповую форму с 2 дочерними формами.
// Мы отрендерим каждую форму в файл изображения в локальной файловой системе
// игнорируя групповые фигуры, так как они не имеют внешнего вида.
// Это создаст 6 файлов изображений.
for (auto&& shape : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> renderer = shape->GetShapeRenderer();
    auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
    renderer->Save(get_ArtifactsDir() + System::String::Format(u"Shape.RenderAllShapes.{0}.png", shape->get_Name()), options);
}
```

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) method


Отрисовывает фигуру в SVG‑изображение и сохраняет в поток.

```cpp
void Aspose::Words::Rendering::NodeRendererBase::Save(const System::SharedPtr<System::IO::Stream> &stream, System::SharedPtr<Aspose::Words::Saving::SvgSaveOptions> saveOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | Поток, в который сохраняется SVG‑изображение формы. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\> | Указывает параметры, которые контролируют, как фигура отображается и сохраняется. Может быть **null**. Если это **null**, изображение будет сохранено с параметрами по умолчанию. |

## Примеры



Показывает, как передать параметры сохранения при рендеринге офисных формул.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

auto options = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
options->set_TextOutputMode(Aspose::Words::Saving::SvgTextOutputMode::UsePlacedGlyphs);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"SvgSaveOptions.Output.svg", options);

{
    auto stream = System::MakeObject<System::IO::MemoryStream>();
    math->GetMathRenderer()->Save(stream, options);
}
```

## См. также

* Class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) method


Отрисовывает фигуру в изображение и сохраняет в файл.

```cpp
void Aspose::Words::Rendering::NodeRendererBase::Save(const System::String &fileName, System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> saveOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | const System::String\& | Имя файла изображения. Если файл с указанным именем уже существует, существующий файл будет перезаписан. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\> | Указывает параметры, которые контролируют, как фигура отображается и сохраняется. Может быть **null**. |

## Примеры



Показывает, как отрендерить объект Office [Math](../../../aspose.words.math/) в файл изображения в локальной файловой системе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// Создайте объект "ImageSaveOptions", чтобы передать его методу "Save" рендерера узла для изменения
// как он рендерит узел OfficeMath в изображение.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// Установите свойство "Scale" в 5, чтобы отрендерить объект в пять раз больше его исходного размера.
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"Shape.RenderOfficeMath.png", saveOptions);
```

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) method


Отрисовывает фигуру в SVG‑изображение и сохраняет в файл.

```cpp
void Aspose::Words::Rendering::NodeRendererBase::Save(const System::String &fileName, System::SharedPtr<Aspose::Words::Saving::SvgSaveOptions> saveOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | const System::String\& | Имя файла изображения. Если файл с указанным именем уже существует, существующий файл будет перезаписан. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\> | Указывает параметры, которые контролируют, как фигура отображается и сохраняется. Может быть **null**. |

## Примеры



Показывает, как передать параметры сохранения при рендеринге офисных формул.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

auto options = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
options->set_TextOutputMode(Aspose::Words::Saving::SvgTextOutputMode::UsePlacedGlyphs);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"SvgSaveOptions.Output.svg", options);

{
    auto stream = System::MakeObject<System::IO::MemoryStream>();
    math->GetMathRenderer()->Save(stream, options);
}
```

## См. также

* Class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Rendering::NodeRendererBase::Save(std::basic_ostream<CharType, Traits> &stream, System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> saveOptions)
```

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Rendering::NodeRendererBase::Save(std::basic_ostream<CharType, Traits> &stream, System::SharedPtr<Aspose::Words::Saving::SvgSaveOptions> saveOptions)
```

## См. также

* Class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
