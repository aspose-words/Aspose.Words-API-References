---
title: "Aspose::Words::DocumentBuilder::InsertOleObject method"
linktitle: "InsertOleObject"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::InsertOleObject method. Вставляет встроенный OLE‑объект из потока в документ на C++."
type: docs
weight: 41000
url: /ru/cpp/aspose.words/documentbuilder/insertoleobject/
---
## DocumentBuilder::InsertOleObject(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Вставляет встроенный объект OLE из потока в документ.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::SharedPtr<System::IO::Stream> &stream, const System::String &progId, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | Поток, содержащий данные приложения. |
| progId | const System::String\& | Программный идентификатор OLE‑объекта. |
| asIcon | bool | Указывает режим вставляемого OLE‑объекта: либо значковый, либо обычный. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Изображение представления OLE‑объекта. Если значение равно **null**, Aspose.Words использует одно из предопределённых изображений. |

### ReturnValue

Узел Shape, содержащий объект Ole, и вставленный в текущую позицию Builder.

## Примеры



Показывает, как использовать документный построитель для встраивания OLE‑объектов в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте таблицу Microsoft Excel из локальной файловой системы
// в документ, сохранив её исходный вид.
{
    System::SharedPtr<System::IO::Stream> spreadsheetStream = System::IO::File::Open(get_MyDir() + u"Spreadsheet.xlsx", System::IO::FileMode::Open);
    builder->Writeln(u"Spreadsheet Ole object:");
    // Если 'presentation' опущен и 'asIcon' установлен, этот перегруженный метод выбирает
    // значок в соответствии с 'progId' и использует предопределённую подпись значка.
    builder->InsertOleObject(spreadsheetStream, u"OleObject.xlsx", false, nullptr);
}

// Вставьте презентацию Microsoft PowerPoint в виде OLE‑объекта.
// На этот раз будет использоваться изображение, загруженное из интернета, в качестве значка.
{
    System::SharedPtr<System::IO::Stream> powerpointStream = System::IO::File::Open(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    System::ArrayPtr<uint8_t> imgBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

    {
        auto imageStream = System::MakeObject<System::IO::MemoryStream>(imgBytes);
        builder->InsertParagraph();
        builder->Writeln(u"Powerpoint Ole object:");
        builder->InsertOleObject(powerpointStream, u"OleObject.pptx", true, imageStream);
    }
}

// Дважды щёлкните эти объекты в Microsoft Word, чтобы открыть
// связанные файлы с помощью соответствующих приложений.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjects.docx");
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Вставляет встроенный или связанный объект OLE из файла в документ. Определяет тип объекта OLE с помощью расширения файла.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::String &fileName, bool isLinked, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | const System::String\& | Полный путь к файлу. |
| isLinked | bool | Если **true**, вставляется связанный OLE‑объект, иначе вставляется встроенный OLE‑объект. |
| asIcon | bool | Указывает режим вставляемого OLE‑объекта: либо значковый, либо обычный. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Изображение представления OLE‑объекта. Если значение равно **null**, Aspose.Words использует одно из предопределённых изображений. |

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
## DocumentBuilder::InsertOleObject(const System::String\&, const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Вставляет встроенный или связанный объект OLE из файла в документ. Определяет тип объекта OLE с помощью указанного параметра progID.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::String &fileName, const System::String &progId, bool isLinked, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | const System::String\& | Полный путь к файлу. |
| progId | const System::String\& | ProgId OLE‑объекта. |
| isLinked | bool | Если **true**, вставляется связанный OLE‑объект, иначе вставляется встроенный OLE‑объект. |
| asIcon | bool | Указывает режим вставляемого OLE‑объекта: либо значковый, либо обычный. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | Изображение представления OLE‑объекта. Если значение равно **null**, Aspose.Words использует одно из предопределённых изображений. |

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
## DocumentBuilder::InsertOleObject(std::basic_istream\<CharType, Traits\>\&, System::String, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(std::basic_istream<CharType, Traits> &stream, System::String progId, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(System::String fileName, bool isLinked, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(System::String, System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(System::String fileName, System::String progId, bool isLinked, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
