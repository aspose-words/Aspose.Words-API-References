---
title: "Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon метод"
linktitle: "InsertOleObjectAsIcon"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon метод. Вставляет встроенный объект OLE в виде значка из потока в документ. Позволяет указать файл значка и подпись. Определяет тип объекта OLE, используя заданный параметр progID в C++."
type: docs
weight: 42000
url: /ru/cpp/aspose.words/documentbuilder/insertoleobjectasicon/
---
## DocumentBuilder::InsertOleObjectAsIcon(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, const System::String\&, const System::String\&) method


Вставляет встроенный объект OLE в виде значка из потока в документ. Позволяет указать файл значка и подпись. Определяет тип объекта OLE с помощью указанного параметра progID.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::SharedPtr<System::IO::Stream> &stream, const System::String &progId, const System::String &iconFile, const System::String &iconCaption)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | Поток, содержащий данные приложения. |
| progId | const System::String\& | ProgId OLE‑объекта. |
| iconFile | const System::String\& | Полный путь к файлу ICO. Если значение **null**, Aspose.Words будет использовать предопределённое изображение. |
| iconCaption | const System::String\& | Подпись значка. Если значение **null**, Aspose.Words будет использовать предопределённую подпись значка. |

### ReturnValue

Узел Shape, содержащий объект Ole, и вставленный в текущую позицию Builder.

## Примеры



Показывает, как вставить встроенный или связанный OLE‑объект в виде значка в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Если 'iconFile' и 'iconCaption' опущены, этот перегруженный метод выбирает
// значок в соответствии с 'progId' и использует имя файла в качестве подписи значка.
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", u"Package", false, get_ImageDir() + u"Logo icon.ico", u"My embedded file");

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    // Если 'iconFile' и 'iconCaption' опущены, этот перегруженный метод выбирает
    // значок в соответствии с расширением файла и использует имя файла в качестве подписи значка.
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObjectAsIcon(stream, u"PowerPoint.Application", get_ImageDir() + u"Logo icon.ico", u"My embedded file stream");

    System::SharedPtr<Aspose::Words::Drawing::OlePackage> setOlePackage = shape->get_OleFormat()->get_OlePackage();
    setOlePackage->set_FileName(u"Presentation.pptx");
    setOlePackage->set_DisplayName(u"Presentation.pptx");
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjectAsIcon.docx");
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObjectAsIcon(const System::String\&, bool, const System::String\&, const System::String\&) method


Вставляет встроенный или связанный объект OLE в виде значка в документ. Позволяет указать файл значка и подпись. Определяет тип объекта OLE с помощью расширения файла.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::String &fileName, bool isLinked, const System::String &iconFile, const System::String &iconCaption)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | const System::String\& | Полный путь к файлу. |
| isLinked | bool | Если **true**, вставляется связанный OLE‑объект, иначе вставляется встроенный OLE‑объект. |
| iconFile | const System::String\& | Полный путь к файлу ICO. Если значение **null**, Aspose.Words будет использовать предопределённое изображение. |
| iconCaption | const System::String\& | Подпись значка. Если значение **null**, Aspose.Words будет использовать имя файла. |

### ReturnValue

Узел Shape, содержащий объект Ole, и вставленный в текущую позицию Builder.

## Примеры



Показывает, как вставить OLE‑объект в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// OLE‑объекты являются ссылками на файлы в нашей локальной файловой системе, которые могут быть открыты другими установленными приложениями.
// Двойной щелчок по этим фигурам запустит приложение, а затем использует его для открытия связанного объекта.
// Существует три способа использования метода InsertOleObject для вставки этих фигур и настройки их внешнего вида.
// 1 –  Изображение, взятое из локальной файловой системы:
{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    // Если 'presentation' опущен и 'asIcon' установлен, этот перегруженный метод выбирает
    // значок в соответствии с расширением файла и использует имя файла в качестве подписи значка.
    builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", false, false, imageStream);
}

// Если 'presentation' опущен и 'asIcon' установлен, этот перегруженный метод выбирает
// значок в соответствии с 'progId' и использует имя файла в качестве подписи значка.
// 2 –  Значок, основанный на приложении, которое откроет объект:
builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", u"Excel.Sheet", false, true, nullptr);

// Если 'iconFile' и 'iconCaption' опущены, этот перегруженный метод выбирает
// значок в соответствии с 'progId' и использует предопределённую подпись значка.
// 3 –  Значок‑изображение размером 32 × 32 пикселя или меньше из локальной файловой системы, с пользовательской подписью:
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", false, get_ImageDir() + u"Logo icon.ico", u"Double click to view presentation!");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObject.docx");
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObjectAsIcon(const System::String\&, const System::String\&, bool, const System::String\&, const System::String\&) method


Вставляет встроенный или связанный объект OLE в виде значка в документ. Позволяет указать файл значка и подпись. Определяет тип объекта OLE с помощью указанного параметра progID.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::String &fileName, const System::String &progId, bool isLinked, const System::String &iconFile, const System::String &iconCaption)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | const System::String\& | Полный путь к файлу. |
| progId | const System::String\& | ProgId OLE‑объекта. |
| isLinked | bool | Если **true**, вставляется связанный OLE‑объект, иначе вставляется встроенный OLE‑объект. |
| iconFile | const System::String\& | Полный путь к файлу ICO. Если значение **null**, Aspose.Words будет использовать предопределённое изображение. |
| iconCaption | const System::String\& | Подпись значка. Если значение **null**, Aspose.Words будет использовать имя файла. |

### ReturnValue

Узел Shape, содержащий объект Ole, и вставленный в текущую позицию Builder.

## Примеры



Показывает, как вставить встроенный или связанный OLE‑объект в виде значка в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Если 'iconFile' и 'iconCaption' опущены, этот перегруженный метод выбирает
// значок в соответствии с 'progId' и использует имя файла в качестве подписи значка.
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", u"Package", false, get_ImageDir() + u"Logo icon.ico", u"My embedded file");

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    // Если 'iconFile' и 'iconCaption' опущены, этот перегруженный метод выбирает
    // значок в соответствии с расширением файла и использует имя файла в качестве подписи значка.
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObjectAsIcon(stream, u"PowerPoint.Application", get_ImageDir() + u"Logo icon.ico", u"My embedded file stream");

    System::SharedPtr<Aspose::Words::Drawing::OlePackage> setOlePackage = shape->get_OleFormat()->get_OlePackage();
    setOlePackage->set_FileName(u"Presentation.pptx");
    setOlePackage->set_DisplayName(u"Presentation.pptx");
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjectAsIcon.docx");
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObjectAsIcon(std::basic_istream\<CharType, Traits\>\&, System::String, System::String, System::String) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(std::basic_istream<CharType, Traits> &stream, System::String progId, System::String iconFile, System::String iconCaption)
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
