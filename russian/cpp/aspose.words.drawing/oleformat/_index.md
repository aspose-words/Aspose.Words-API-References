---
title: "Класс Aspose::Words::Drawing::OleFormat"
linktitle: "OleFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Drawing::OleFormat. Предоставляет доступ к данным OLE-объекта или элемента управления ActiveX. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.drawing/oleformat/
---
## OleFormat class


Обеспечивает доступ к данным OLE‑объекта или элемента управления ActiveX. Чтобы узнать больше, посетите статью документации [Working with Ole Objects](https://docs.aspose.com/words/cpp/working-with-ole-objects/) .

```cpp
class OleFormat : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_AutoUpdate](./get_autoupdate/)() | Указывает, автоматически обновляется ссылка на OLE-объект в Microsoft Word или нет. |
| [get_Clsid](./get_clsid/)() | Получает CLSID OLE-объекта. |
| [get_IconCaption](./get_iconcaption/)() | Получает подпись значка OLE-объекта. Если у OLE-объекта нет значка или подпись не может быть получена, возвращает пустую строку. |
| [get_IsLink](./get_islink/)() | Возвращает **true**, если OLE-объект связан (когда указано [SourceFullName](./get_sourcefullname/)). |
| [get_IsLocked](./get_islocked/)() | Указывает, заблокирована ли ссылка на OLE-объект от обновлений. |
| [get_OleControl](./get_olecontrol/)() | Получает объекты [OleControl](./get_olecontrol/), если этот OLE-объект является элементом управления ActiveX. В противном случае это свойство равно null. |
| [get_OleIcon](./get_oleicon/)() | Получает аспект отображения OLE-объекта. Когда **true**, OLE-объект отображается как значок. Когда **false**, OLE-объект отображается как содержимое. |
| [get_OlePackage](./get_olepackage/)() | Обеспечивает доступ к [OlePackage](../olepackage/), если OLE-объект является OLE Package. В противном случае возвращает **null**. |
| [get_ProgId](./get_progid/)() | Получает или задает ProgID OLE-объекта. |
| [get_SourceFullName](./get_sourcefullname/)() | Получает или задает путь и имя исходного файла для связанного OLE-объекта. |
| [get_SourceItem](./get_sourceitem/)() | Получает или задает строку, используемую для идентификации части исходного файла, которая связывается. |
| [get_SuggestedExtension](./get_suggestedextension/)() | Получает рекомендуемое расширение файла для текущего встроенного объекта, если вы хотите сохранить его в файл. |
| [get_SuggestedFileName](./get_suggestedfilename/)() | Получает рекомендуемое имя файла для текущего встроенного объекта, если вы хотите сохранить его в файл. |
| [GetOleEntry](./getoleentry/)(const System::String\&) | Получает запись данных OLE-объекта. |
| [GetRawData](./getrawdata/)() | Получает необработанные данные OLE-объекта. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Сохраняет данные встроенного объекта в указанный поток. |
| [Save](./save/)(const System::String\&) | Сохраняет данные встроенного объекта в файл с указанным именем. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_AutoUpdate](./set_autoupdate/)(bool) | Сеттер для [Aspose::Words::Drawing::OleFormat::get_AutoUpdate](./get_autoupdate/). |
| [set_IsLocked](./set_islocked/)(bool) | Сеттер для [Aspose::Words::Drawing::OleFormat::get_IsLocked](./get_islocked/). |
| [set_ProgId](./set_progid/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::OleFormat::get_ProgId](./get_progid/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::OleFormat::get_SourceFullName](./get_sourcefullname/). |
| [set_SourceItem](./set_sourceitem/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::OleFormat::get_SourceItem](./get_sourceitem/). |
| static [Type](./type/)() |  |
## Примечания


Используйте свойство [OleFormat](../shape/get_oleformat/) для доступа к данным OLE‑объекта. Вы не создаёте экземпляры класса [OleFormat](./) напрямую.

## Примеры



Показывает, как извлекать встроенные OLE‑объекты в файлы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE spreadsheet.docm");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// OLE‑объект в первой фигуре представляет собой таблицу Microsoft Excel.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shape->get_OleFormat();

ASSERT_EQ(u"Excel.Sheet.12", oleFormat->get_ProgId());

// Наш объект не обновляется автоматически и не заблокирован от обновлений.
ASSERT_FALSE(oleFormat->get_AutoUpdate());
ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLocked());

// Если мы планируем сохранять OLE‑объект в файл в локальной файловой системе,
// мы можем использовать свойство "SuggestedExtension", чтобы определить, какое расширение файла применить.
ASSERT_EQ(u".xlsx", oleFormat->get_SuggestedExtension());

// Ниже представлены два способа сохранения OLE‑объекта в файл в локальной файловой системе.
// 1 -  Сохранить через поток:
{
    auto fs = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"OLE spreadsheet extracted via stream" + oleFormat->get_SuggestedExtension(), System::IO::FileMode::Create);
    oleFormat->Save(fs);
}

// 2 -  Сохранить напрямую в файл:
oleFormat->Save(get_ArtifactsDir() + u"OLE spreadsheet saved directly" + oleFormat->get_SuggestedExtension());
```

## См. также

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
